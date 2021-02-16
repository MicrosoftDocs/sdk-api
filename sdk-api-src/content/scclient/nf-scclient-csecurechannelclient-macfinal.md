---
UID: NF:scclient.CSecureChannelClient.MACFinal
title: CSecureChannelClient::MACFinal (scclient.h)
description: The MACFinal method releases the message authentication code (MAC) channel and retrieves a final MAC value.
helpviewer_keywords: ["CSecureChannelClient class [windows Media Device Manager]","MACFinal method","CSecureChannelClient.MACFinal","CSecureChannelClient::MACFinal","CSecureChannelClientMACFinal","MACFinal","MACFinal method [windows Media Device Manager]","MACFinal method [windows Media Device Manager]","CSecureChannelClient class","scclient/CSecureChannelClient::MACFinal","wmdm.csecurechannelclient_macfinal"]
old-location: wmdm\csecurechannelclient_macfinal.htm
tech.root: WMDM
ms.assetid: 64dc8e36-c135-415f-a646-04919e4d031d
ms.date: 12/05/2018
ms.keywords: CSecureChannelClient class [windows Media Device Manager],MACFinal method, CSecureChannelClient.MACFinal, CSecureChannelClient::MACFinal, CSecureChannelClientMACFinal, MACFinal, MACFinal method [windows Media Device Manager], MACFinal method [windows Media Device Manager],CSecureChannelClient class, scclient/CSecureChannelClient::MACFinal, wmdm.csecurechannelclient_macfinal
req.header: scclient.h
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
 - CSecureChannelClient::MACFinal
 - scclient/CSecureChannelClient::MACFinal
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
 - CSecureChannelClient.MACFinal
---

# CSecureChannelClient::MACFinal


## -description

The <b>MACFinal</b> method releases the message authentication code (MAC) channel and retrieves a final MAC value.

## -parameters

### -param hMAC [in]

Handle for the MAC for the current parameter data. This handle is created by calling the <b>MACInit</b> method. This datatype is declared in the SDK file ...\inc\Sac.h. After this method is called, the handle passed in is no longer valid.

### -param abData [out]

Array of bytes to receive the final MAC value for the current parameter data.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td>S_OK</td>
<td>The method succeeded.</td>
</tr>
<tr>
<td>E_INVALIDARG</td>
<td>A parameter is invalid.</td>
</tr>
<tr>
<td>E_FAIL</td>
<td>An unspecified error occurred.</td>
</tr>
</table>

## -remarks

This method completes creating a MAC key. For information about MAC creation, see <a href="/windows/desktop/WMDM/message-authentication">Message Authentication</a>.


#### Examples

The following example code checks the MAC received by a call to <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getrights">IWMDMStorage::GetRights</a> to verify that the data has not been tampered with.


```cpp

HRESULT hr;
CSecureChannelClient *pSPClient = NULL;
hr = m_pStorage->GetRights(ppRights, pnRightsCount, abTempMAC);
if (SUCCEEDED(hr))
{
    // Verify MAC returned by GetRights on the service provider.
    pSPClient->MACInit(&hMAC);
    pSPClient->MACUpdate(hMAC, (BYTE*)(*ppRights),
                       sizeof(WMDMRIGHTS) * (*pnRightsCount));
    pSPClient->MACUpdate(hMAC, (BYTE*)(pnRightsCount),
                        sizeof(*pnRightsCount));
    pSPClient->MACFinal(hMAC, abMACVerify);
    if (memcmp(abMACVerify, abTempMAC, WMDM_MAC_LENGTH) != 0)
    {
        hr = WMDM_E_MAC_CHECK_FAILED;
        goto exit;
    }
}

```

## -see-also

<a href="/windows/desktop/WMDM/csecurechannelclient-class">CSecureChannelClient Class</a>



<a href="/previous-versions/bb231593(v=vs.85)">CSecureChannelClient::MACUpdate</a>



<a href="/windows/desktop/WMDM/message-authentication">Message Authentication</a>