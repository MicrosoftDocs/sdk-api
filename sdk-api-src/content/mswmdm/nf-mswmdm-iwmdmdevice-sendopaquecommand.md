---
UID: NF:mswmdm.IWMDMDevice.SendOpaqueCommand
title: IWMDMDevice::SendOpaqueCommand (mswmdm.h)
description: The SendOpaqueCommand method sends a device-specific command to the device through Windows Media Device Manager. Windows Media Device Manager does not attempt to read the command.
helpviewer_keywords: ["IWMDMDevice interface [windows Media Device Manager]","SendOpaqueCommand method","IWMDMDevice.SendOpaqueCommand","IWMDMDevice::SendOpaqueCommand","IWMDMDeviceSendOpaqueCommand","SendOpaqueCommand","SendOpaqueCommand method [windows Media Device Manager]","SendOpaqueCommand method [windows Media Device Manager]","IWMDMDevice interface","mswmdm/IWMDMDevice::SendOpaqueCommand","wmdm.iwmdmdevice_sendopaquecommand"]
old-location: wmdm\iwmdmdevice_sendopaquecommand.htm
tech.root: WMDM
ms.assetid: 4554318b-497f-488f-a52f-a392b8fee992
ms.date: 12/05/2018
ms.keywords: IWMDMDevice interface [windows Media Device Manager],SendOpaqueCommand method, IWMDMDevice.SendOpaqueCommand, IWMDMDevice::SendOpaqueCommand, IWMDMDeviceSendOpaqueCommand, SendOpaqueCommand, SendOpaqueCommand method [windows Media Device Manager], SendOpaqueCommand method [windows Media Device Manager],IWMDMDevice interface, mswmdm/IWMDMDevice::SendOpaqueCommand, wmdm.iwmdmdevice_sendopaquecommand
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
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMDMDevice::SendOpaqueCommand
 - mswmdm/IWMDMDevice::SendOpaqueCommand
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mssachlp.lib
 - mssachlp.dll
api_name:
 - IWMDMDevice.SendOpaqueCommand
---

# IWMDMDevice::SendOpaqueCommand


## -description

The <b>SendOpaqueCommand</b> method sends a device-specific command to the device through Windows Media Device Manager. Windows Media Device Manager does not attempt to read the command.

## -parameters

### -param pCommand [in, out]

Pointer to an <a href="/windows/desktop/WMDM/opaquecommand">OPAQUECOMMAND</a> structure specifying the information required to execute the command. If the device returns data, it is returned through the <i>pData</i> member of <i>pCommand</i>.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

This method is intended for device commands that do not affect the operation of Windows Media Device Manager and are passed through unchanged.


#### Examples

The following code performs a simplified extended authentication procedure with a device. This procedure is specific to a device.


```cpp

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
        memcpy(&(Command.guidCommand), &guidCertInfoEx, sizeof(GUID));

        Command.pData = (BYTE *)CoTaskMemAlloc(cbData_Send);
        if (!Command.pData)
        {
            ExitOnFail(hr = E_OUTOFMEMORY);
        }
        Command.dwDataLen = cbData_Send;

        // Map the data in the opaque command to a CERTINFOEX structure, and
        // fill in the certificate info to send.
        pCertInfoEx = (CERTINFOEX *)Command.pData;

        pCertInfoEx->hr     = S_OK;
        pCertInfoEx->cbCert = cbData_App;
        memcpy(pCertInfoEx->pbCert, bCertInfoEx_App, cbData_App);

        // Compute the MAC to send.
        g_cWmdm.m_pSAC->MACInit(&hMAC);
        g_cWmdm.m_pSAC->MACUpdate(hMAC, (BYTE*)(&(Command.guidCommand)), sizeof(GUID));
        g_cWmdm.m_pSAC->MACUpdate(hMAC, (BYTE*)(&(Command.dwDataLen)), sizeof(Command.dwDataLen));
        if (Command.pData)
        {
            g_cWmdm.m_pSAC->MACUpdate(hMAC, Command.pData, Command.dwDataLen);
        }
        g_cWmdm.m_pSAC->MACFinal(hMAC, Command.abMAC);

        // Send the command.
        hr = pDevice->SendOpaqueCommand(&Command);
        if (SUCCEEDED(hr))
        {
            BYTE abMACVerify2[ WMDM_MAC_LENGTH ];

            // Compute retrieved MAC for verification.
            g_cWmdm.m_pSAC->MACInit(&hMAC);
            g_cWmdm.m_pSAC->MACUpdate(hMAC, (BYTE*)(&(Command.guidCommand)), sizeof(GUID));
            g_cWmdm.m_pSAC->MACUpdate(hMAC, (BYTE*)(&(Command.dwDataLen)), sizeof(Command.dwDataLen));
            if (Command.pData)
            {
                g_cWmdm.m_pSAC->MACUpdate(hMAC, Command.pData, Command.dwDataLen);
            }
            g_cWmdm.m_pSAC->MACFinal(hMAC, abMACVerify2);

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
                if ((pCertInfoEx->cbCert != cbData_SP) ||
                    (memcmp(pCertInfoEx->pbCert, bCertInfoEx_SP, cbData_SP) == 0))
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

```

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice">IWMDMDevice Interface</a>