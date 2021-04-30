---
UID: NF:mswmdm.IWMDMStorage.SendOpaqueCommand
title: IWMDMStorage::SendOpaqueCommand (mswmdm.h)
description: The SendOpaqueCommand method sends a command to the storage through Windows Media Device Manager, without processing it.
helpviewer_keywords: ["IWMDMStorage interface [windows Media Device Manager]","SendOpaqueCommand method","IWMDMStorage.SendOpaqueCommand","IWMDMStorage::SendOpaqueCommand","IWMDMStorageSendOpaqueCommand","SendOpaqueCommand","SendOpaqueCommand method [windows Media Device Manager]","SendOpaqueCommand method [windows Media Device Manager]","IWMDMStorage interface","mswmdm/IWMDMStorage::SendOpaqueCommand","wmdm.iwmdmstorage_sendopaquecommand"]
old-location: wmdm\iwmdmstorage_sendopaquecommand.htm
tech.root: WMDM
ms.assetid: a5e570ad-63d3-4c8f-8569-63aa3645f866
ms.date: 12/05/2018
ms.keywords: IWMDMStorage interface [windows Media Device Manager],SendOpaqueCommand method, IWMDMStorage.SendOpaqueCommand, IWMDMStorage::SendOpaqueCommand, IWMDMStorageSendOpaqueCommand, SendOpaqueCommand, SendOpaqueCommand method [windows Media Device Manager], SendOpaqueCommand method [windows Media Device Manager],IWMDMStorage interface, mswmdm/IWMDMStorage::SendOpaqueCommand, wmdm.iwmdmstorage_sendopaquecommand
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
 - IWMDMStorage::SendOpaqueCommand
 - mswmdm/IWMDMStorage::SendOpaqueCommand
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
 - IWMDMStorage.SendOpaqueCommand
---

# IWMDMStorage::SendOpaqueCommand


## -description

The <b>SendOpaqueCommand</b> method sends a command to the storage through Windows Media Device Manager, without processing it.

## -parameters

### -param pCommand [in, out]

Pointer to an <a href="/windows/desktop/WMDM/opaquecommand">OPAQUECOMMAND</a> structure containing the command to execute. Data can be passed two ways—from the application to the device, and from the device back to the application when the call finishes.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

This method is intended for storage media commands that do not affect the operation of Windows Media Device Manager and should be passed through unchanged.


#### Examples

The following C++ code calls <b>SendOpaqueCommand</b> to perform a simple custom authentication step with a device. The caller sends its certificate and MAC to the device, which sends back its own certificate and MAC. The application compares the retrieved certificate with the one it has stored, and if they match (and the MAC is correct), it sets bExtraCertified to <b>TRUE</b>.


```cpp

    // Call SendOpaqueCommand to exchange extended authentication information.
    {
        HMAC           hMAC;
        OPAQUECOMMAND  Command;
        CERTINFOEX    *pCertInfoEx;
        DWORD          cbData_App   = sizeof(bCertInfoEx_App)/sizeof(bCertInfoEx_App[0]);
        DWORD          cbData_SP    = sizeof(bCertInfoEx_SP)/sizeof(bCertInfoEx_SP[0]);
        DWORD          cbData_Send  = sizeof(CERTINFOEX) + cbData_App;

        // Fill opaque command structure with the application's certificate.
        memcpy(&(Command.guidCommand), &guidCertInfoEx, sizeof(GUID));

        Command.pData = (BYTE *)CoTaskMemAlloc(cbData_Send);
        if (!Command.pData)
        {
            ExitOnFail(hr = E_OUTOFMEMORY);
        }
        Command.dwDataLen = cbData_Send;

        // Map the data in the opaque command to a CERTINFOEX structure, and
        // fill in the cert info to send.
        pCertInfoEx = (CERTINFOEX *)Command.pData;
        pCertInfoEx->hr     = S_OK;
        pCertInfoEx->cbCert = cbData_App;
        memcpy(pCertInfoEx->pbCert, bCertInfoEx_App, cbData_App);

        // Compute MAC on the data, and add to the OPAQUECOMMAND struct.
        g_cWmdm.m_pSAC->MACInit(&hMAC);
        g_cWmdm.m_pSAC->MACUpdate(hMAC, (BYTE*)(&(Command.guidCommand)), sizeof(GUID));
        g_cWmdm.m_pSAC->MACUpdate(hMAC, (BYTE*)(&(Command.dwDataLen)), sizeof(Command.dwDataLen));
        if (Command.pData)
        {
            g_cWmdm.m_pSAC->MACUpdate(hMAC, Command.pData, Command.dwDataLen);
        }
        g_cWmdm.m_pSAC->MACFinal(hMAC, Command.abMAC);

        // Send the opaque command.
        hr = pDevice->SendOpaqueCommand(&Command);
        if (SUCCEEDED(hr))
        {
            // Now verify the retrieved MAC.
            BYTE abMACVerify2[ WMDM_MAC_LENGTH ];
            g_cWmdm.m_pSAC->MACInit(&hMAC);
            g_cWmdm.m_pSAC->MACUpdate(hMAC, (BYTE*)(&(Command.guidCommand)), sizeof(GUID));
            g_cWmdm.m_pSAC->MACUpdate(hMAC, (BYTE*)(&(Command.dwDataLen)), sizeof(Command.dwDataLen));
            if (Command.pData)
            {
                g_cWmdm.m_pSAC->MACUpdate(hMAC, Command.pData, Command.dwDataLen);
            }
            g_cWmdm.m_pSAC->MACFinal(hMAC, abMACVerify2);

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
                if ((pCertInfoEx->cbCert != cbData_SP) &&
                    (memcmp(pCertInfoEx->pbCert, bCertInfoEx_SP, cbData_SP) == 0))
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

```

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage">IWMDMStorage Interface</a>