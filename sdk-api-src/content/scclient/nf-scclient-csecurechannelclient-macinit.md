---
UID: NF:scclient.CSecureChannelClient.MACInit
title: CSecureChannelClient::MACInit (scclient.h)
description: The MACInit method acquires a message authentication code (MAC) channel.
helpviewer_keywords: ["CSecureChannelClient class [windows Media Device Manager]","MACInit method","CSecureChannelClient.MACInit","CSecureChannelClient::MACInit","CSecureChannelClientMACInit","MACInit","MACInit method [windows Media Device Manager]","MACInit method [windows Media Device Manager]","CSecureChannelClient class","scclient/CSecureChannelClient::MACInit","wmdm.csecurechannelclient_macinit"]
old-location: wmdm\csecurechannelclient_macinit.htm
tech.root: WMDM
ms.assetid: d383d040-55f7-4ed7-b5b8-8e963b6cb16a
ms.date: 12/05/2018
ms.keywords: CSecureChannelClient class [windows Media Device Manager],MACInit method, CSecureChannelClient.MACInit, CSecureChannelClient::MACInit, CSecureChannelClientMACInit, MACInit, MACInit method [windows Media Device Manager], MACInit method [windows Media Device Manager],CSecureChannelClient class, scclient/CSecureChannelClient::MACInit, wmdm.csecurechannelclient_macinit
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
 - CSecureChannelClient::MACInit
 - scclient/CSecureChannelClient::MACInit
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
 - CSecureChannelClient.MACInit
---

# CSecureChannelClient::MACInit


## -description

The <b>MACInit</b> method acquires a message authentication code (MAC) channel.

## -parameters

### -param phMAC [out]

Pointer to the MAC handle for the parameter data. The handle is acquired by <b>MACInit</b> to be used for subsequent <a href="/previous-versions/bb231593(v=vs.85)">MACUpdate</a> and <a href="/previous-versions/bb231591(v=vs.85)">MACFinal</a> calls. This datatype is declared in Sac.h installed with the Windows Media Format SDK.

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
<td>The phMAC parameter is invalid or is a <b>NULL</b> pointer.</td>
</tr>
<tr>
<td>E_FAIL</td>
<td>An unspecified error occurred.</td>
</tr>
</table>

## -remarks

<b>MACInit</b> begins a message authentication code (MAC) session. For example, <b>MACInit</b> should be called before content is transferred when writing to a storage device to verify the MAC returned by the <a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-getrights">IMDSPStorage::GetRights</a> call on the service provider.


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



<a href="/previous-versions/bb231591(v=vs.85)">CSecureChannelClient::MACFinal</a>



<a href="/previous-versions/bb231593(v=vs.85)">CSecureChannelClient::MACUpdate</a>



<a href="/windows/desktop/WMDM/message-authentication">Message Authentication</a>