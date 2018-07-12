---
UID: NF:mswmdm.IWMDMStorage.SendOpaqueCommand
title: IWMDMStorage::SendOpaqueCommand
author: windows-sdk-content
description: The SendOpaqueCommand method sends a command to the storage through Windows Media Device Manager, without processing it.
old-location: wmdm\iwmdmstorage_sendopaquecommand.htm
old-project: WMDM
ms.assetid: a5e570ad-63d3-4c8f-8569-63aa3645f866
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: IWMDMStorage interface [windows Media Device Manager],SendOpaqueCommand method, IWMDMStorage.SendOpaqueCommand, IWMDMStorage::SendOpaqueCommand, IWMDMStorageSendOpaqueCommand, SendOpaqueCommand, SendOpaqueCommand method [windows Media Device Manager], SendOpaqueCommand method [windows Media Device Manager],IWMDMStorage interface, mswmdm/IWMDMStorage::SendOpaqueCommand, wmdm.iwmdmstorage_sendopaquecommand
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MSVidCtlStateList
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mssachlp.lib
 - mssachlp.dll
api_name:
 - IWMDMStorage.SendOpaqueCommand
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IWMDMStorage::SendOpaqueCommand


## -description



The <b>SendOpaqueCommand</b> method sends a command to the storage through Windows Media Device Manager, without processing it.




## -parameters




### -param pCommand [in, out]

Pointer to an <a href="https://msdn.microsoft.com/5b39cf07-2816-4615-a754-e3f0c57bf4ce">OPAQUECOMMAND</a> structure containing the command to execute. Data can be passed two ways—from the application to the device, and from the device back to the application when the call finishes.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn938542">Error Codes</a>.




## -remarks



This method is intended for storage media commands that do not affect the operation of Windows Media Device Manager and should be passed through unchanged.


#### Examples

The following C++ code calls <b>SendOpaqueCommand</b> to perform a simple custom authentication step with a device. The caller sends its certificate and MAC to the device, which sends back its own certificate and MAC. The application compares the retrieved certificate with the one it has stored, and if they match (and the MAC is correct), it sets bExtraCertified to <b>TRUE</b>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
    // Call SendOpaqueCommand to exchange extended authentication information.
    {
        HMAC           hMAC;
        OPAQUECOMMAND  Command;
        CERTINFOEX    *pCertInfoEx;
        DWORD          cbData_App   = sizeof(bCertInfoEx_App)/sizeof(bCertInfoEx_App[0]);
        DWORD          cbData_SP    = sizeof(bCertInfoEx_SP)/sizeof(bCertInfoEx_SP[0]);
        DWORD          cbData_Send  = sizeof(CERTINFOEX) + cbData_App;

        // Fill opaque command structure with the application's certificate.
        memcpy(&amp;(Command.guidCommand), &amp;guidCertInfoEx, sizeof(GUID));

        Command.pData = (BYTE *)CoTaskMemAlloc(cbData_Send);
        if (!Command.pData)
        {
            ExitOnFail(hr = E_OUTOFMEMORY);
        }
        Command.dwDataLen = cbData_Send;

        // Map the data in the opaque command to a CERTINFOEX structure, and
        // fill in the cert info to send.
        pCertInfoEx = (CERTINFOEX *)Command.pData;
        pCertInfoEx-&gt;hr     = S_OK;
        pCertInfoEx-&gt;cbCert = cbData_App;
        memcpy(pCertInfoEx-&gt;pbCert, bCertInfoEx_App, cbData_App);

        // Compute MAC on the data, and add to the OPAQUECOMMAND struct.
        g_cWmdm.m_pSAC-&gt;MACInit(&amp;hMAC);
        g_cWmdm.m_pSAC-&gt;MACUpdate(hMAC, (BYTE*)(&amp;(Command.guidCommand)), sizeof(GUID));
        g_cWmdm.m_pSAC-&gt;MACUpdate(hMAC, (BYTE*)(&amp;(Command.dwDataLen)), sizeof(Command.dwDataLen));
        if (Command.pData)
        {
            g_cWmdm.m_pSAC-&gt;MACUpdate(hMAC, Command.pData, Command.dwDataLen);
        }
        g_cWmdm.m_pSAC-&gt;MACFinal(hMAC, Command.abMAC);

        // Send the opaque command.
        hr = pDevice-&gt;SendOpaqueCommand(&amp;Command);
        if (SUCCEEDED(hr))
        {
            // Now verify the retrieved MAC.
            BYTE abMACVerify2[ WMDM_MAC_LENGTH ];
            g_cWmdm.m_pSAC-&gt;MACInit(&amp;hMAC);
            g_cWmdm.m_pSAC-&gt;MACUpdate(hMAC, (BYTE*)(&amp;(Command.guidCommand)), sizeof(GUID));
            g_cWmdm.m_pSAC-&gt;MACUpdate(hMAC, (BYTE*)(&amp;(Command.dwDataLen)), sizeof(Command.dwDataLen));
            if (Command.pData)
            {
                g_cWmdm.m_pSAC-&gt;MACUpdate(hMAC, Command.pData, Command.dwDataLen);
            }
            g_cWmdm.m_pSAC-&gt;MACFinal(hMAC, abMACVerify2);

            // Verify MAC matches.
            if (memcmp(abMACVerify2, Command.abMAC, WMDM_MAC_LENGTH) == 0)
            {
                 // They match; verify the retrieved certificate.
                // Map the data in the opaque command to a CERTINFOEX structure
                //
                pCertInfoEx = (CERTINFOEX *)Command.pData;

                // In this simple extended authentication scheme, the callee must
                // provide the exact certificate information.
                //
                if ((pCertInfoEx-&gt;cbCert != cbData_SP) &amp;&amp;
                    (memcmp(pCertInfoEx-&gt;pbCert, bCertInfoEx_SP, cbData_SP) == 0))
                {
                    bExtraCertified = TRUE;
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




<a href="https://msdn.microsoft.com/1ede7c68-0169-4375-9b45-b0995ad14e44">IWMDMStorage Interface</a>
 

 

