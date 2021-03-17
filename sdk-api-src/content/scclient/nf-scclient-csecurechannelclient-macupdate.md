---
UID: NF:scclient.CSecureChannelClient.MACUpdate
title: CSecureChannelClient::MACUpdate (scclient.h)
description: The MACUpdate method adds a value to a message authentication code (MAC).
helpviewer_keywords: ["CSecureChannelClient class [windows Media Device Manager]","MACUpdate method","CSecureChannelClient.MACUpdate","CSecureChannelClient::MACUpdate","CSecureChannelClientMACUpdate","MACUpdate","MACUpdate method [windows Media Device Manager]","MACUpdate method [windows Media Device Manager]","CSecureChannelClient class","scclient/CSecureChannelClient::MACUpdate","wmdm.csecurechannelclient_macupdate"]
old-location: wmdm\csecurechannelclient_macupdate.htm
tech.root: WMDM
ms.assetid: b868d422-535d-44f5-9713-bfa049da8a4e
ms.date: 12/05/2018
ms.keywords: CSecureChannelClient class [windows Media Device Manager],MACUpdate method, CSecureChannelClient.MACUpdate, CSecureChannelClient::MACUpdate, CSecureChannelClientMACUpdate, MACUpdate, MACUpdate method [windows Media Device Manager], MACUpdate method [windows Media Device Manager],CSecureChannelClient class, scclient/CSecureChannelClient::MACUpdate, wmdm.csecurechannelclient_macupdate
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
 - CSecureChannelClient::MACUpdate
 - scclient/CSecureChannelClient::MACUpdate
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
 - CSecureChannelClient.MACUpdate
---

# CSecureChannelClient::MACUpdate


## -description

The <b>MACUpdate</b> method adds a value to a message authentication code (MAC).

## -parameters

### -param hMAC [in]

Handle to the array specifying the MAC for the current parameter data. This handle is returned from the <a href="/previous-versions/bb231592(v=vs.85)">MACInit</a> method. This datatype is declared in Sac.h installed with the Windows Media Format SDK.

### -param pbData [in]

Pointer to the parameter data to add to the MAC value.

### -param dwDataLen

<b>DWORD</b> specifying the length of the data to which <i>pbData</i> points.

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
<td>A parameter is invalid or is a <b>NULL</b> pointer.</td>
</tr>
<tr>
<td>E_FAIL</td>
<td>An unspecified error occurred.</td>
</tr>
</table>

## -remarks

An application calls <b>MACUpdate</b> repeatedly with each piece of data to add to the MAC. <b>MACInit</b> must always be called before <b>MACUpdate</b>, and <a href="/previous-versions/bb231591(v=vs.85)">MACFinal</a> must always be called after <b>MACUpdate</b>. <b>MACInit</b> acquires the MAC handle, <b>phMAC</b>, to be used by the <b>MACUpdate</b> and <b>MACFinal</b> methods.


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



<a href="/windows/desktop/WMDM/message-authentication">Message Authentication</a>