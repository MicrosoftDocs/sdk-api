---
UID: NF:mswmdm.IWMDMDevice.SendOpaqueCommand
title: IWMDMDevice::SendOpaqueCommand
author: windows-driver-content
description: The SendOpaqueCommand method sends a device-specific command to the device through Windows Media Device Manager. Windows Media Device Manager does not attempt to read the command.
old-location: wmdm\iwmdmdevice_sendopaquecommand.htm
old-project: WMDM
ms.assetid: 4554318b-497f-488f-a52f-a392b8fee992
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: IWMDMDevice interface [windows Media Device Manager],SendOpaqueCommand method, IWMDMDevice.SendOpaqueCommand, IWMDMDevice::SendOpaqueCommand, IWMDMDeviceSendOpaqueCommand, SendOpaqueCommand, SendOpaqueCommand method [windows Media Device Manager], SendOpaqueCommand method [windows Media Device Manager],IWMDMDevice interface, mswmdm/IWMDMDevice::SendOpaqueCommand, wmdm.iwmdmdevice_sendopaquecommand
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mswmdm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MSVidCtlStateList
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mssachlp.lib
-	mssachlp.dll
api_name:
-	IWMDMDevice.SendOpaqueCommand
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IWMDMDevice::SendOpaqueCommand


## -description



The <b>SendOpaqueCommand</b> method sends a device-specific command to the device through Windows Media Device Manager. Windows Media Device Manager does not attempt to read the command.




## -parameters




### -param pCommand [in, out]

Pointer to an <a href="https://msdn.microsoft.com/5b39cf07-2816-4615-a754-e3f0c57bf4ce">OPAQUECOMMAND</a> structure specifying the information required to execute the command. If the device returns data, it is returned through the <i>pData</i> member of <i>pCommand</i>.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn938542">Error Codes</a>.




## -remarks



This method is intended for device commands that do not affect the operation of Windows Media Device Manager and are passed through unchanged.


#### Examples

The following code performs a simplified extended authentication procedure with a device. This procedure is specific to a device.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
// Call opaque command to exchange extended authentication information.
    //
    {
        HMAC           hMAC;
        OPAQUECOMMAND  Command;
        CERTINFOEX    *pCertInfoEx;
        DWORD          cbData_App   = sizeof(bCertInfoEx_App)/sizeof(bCertInfoEx_App[0]);
        DWORD          cbData_SP    = sizeof(bCertInfoEx_SP)/sizeof(bCertInfoEx_SP[0]);
        DWORD          cbData_Send  = sizeof(CERTINFOEX) + cbData_App;

        // Fill out opaque command structure.
        memcpy(&amp;(Command.guidCommand), &amp;guidCertInfoEx, sizeof(GUID));

        Command.pData = (BYTE *)CoTaskMemAlloc(cbData_Send);
        if (!Command.pData)
        {
            ExitOnFail(hr = E_OUTOFMEMORY);
        }
        Command.dwDataLen = cbData_Send;

        // Map the data in the opaque command to a CERTINFOEX structure, and
        // fill in the certificate info to send.
        pCertInfoEx = (CERTINFOEX *)Command.pData;

        pCertInfoEx-&gt;hr     = S_OK;
        pCertInfoEx-&gt;cbCert = cbData_App;
        memcpy(pCertInfoEx-&gt;pbCert, bCertInfoEx_App, cbData_App);

        // Compute the MAC to send.
        g_cWmdm.m_pSAC-&gt;MACInit(&amp;hMAC);
        g_cWmdm.m_pSAC-&gt;MACUpdate(hMAC, (BYTE*)(&amp;(Command.guidCommand)), sizeof(GUID));
        g_cWmdm.m_pSAC-&gt;MACUpdate(hMAC, (BYTE*)(&amp;(Command.dwDataLen)), sizeof(Command.dwDataLen));
        if (Command.pData)
        {
            g_cWmdm.m_pSAC-&gt;MACUpdate(hMAC, Command.pData, Command.dwDataLen);
        }
        g_cWmdm.m_pSAC-&gt;MACFinal(hMAC, Command.abMAC);

        // Send the command.
        hr = pDevice-&gt;SendOpaqueCommand(&amp;Command);
        if (SUCCEEDED(hr))
        {
            BYTE abMACVerify2[ WMDM_MAC_LENGTH ];

            // Compute retrieved MAC for verification.
            g_cWmdm.m_pSAC-&gt;MACInit(&amp;hMAC);
            g_cWmdm.m_pSAC-&gt;MACUpdate(hMAC, (BYTE*)(&amp;(Command.guidCommand)), sizeof(GUID));
            g_cWmdm.m_pSAC-&gt;MACUpdate(hMAC, (BYTE*)(&amp;(Command.dwDataLen)), sizeof(Command.dwDataLen));
            if (Command.pData)
            {
                g_cWmdm.m_pSAC-&gt;MACUpdate(hMAC, Command.pData, Command.dwDataLen);
            }
            g_cWmdm.m_pSAC-&gt;MACFinal(hMAC, abMACVerify2);

            // Verify the MAC matches.
            //
            if (memcmp(abMACVerify2, Command.abMAC, WMDM_MAC_LENGTH) == 0)
            {
                // Cast the data in the opaque command to a CERTINFOEX structure.
                //
                pCertInfoEx = (CERTINFOEX *)Command.pData;

                // In this simple extended authentication scheme, the callee must
                // provide the exact certificate info.
                //
                if ((pCertInfoEx-&gt;cbCert != cbData_SP) ||
                    (memcmp(pCertInfoEx-&gt;pbCert, bCertInfoEx_SP, cbData_SP) == 0))
                {
                    m_fExtraCertified = TRUE;
                }
            }
        }

        if (Command.pData)
        {
            CoTaskMemFree(Command.pData);
        }
    }
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/44212da9-a38a-4ed5-86af-cf60b40bb54d">IWMDMDevice Interface</a>
 

 

