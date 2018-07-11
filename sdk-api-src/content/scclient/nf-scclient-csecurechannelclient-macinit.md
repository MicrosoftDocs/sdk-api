---
UID: NF:scclient.CSecureChannelClient.MACInit
title: CSecureChannelClient::MACInit
author: windows-sdk-content
description: The MACInit method acquires a message authentication code (MAC) channel.
old-location: wmdm\csecurechannelclient_macinit.htm
old-project: WMDM
ms.assetid: d383d040-55f7-4ed7-b5b8-8e963b6cb16a
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: CSecureChannelClient interface [windows Media Device Manager],MACInit method, CSecureChannelClient.MACInit, CSecureChannelClient::MACInit, CSecureChannelClientMACInit, MACInit, MACInit method [windows Media Device Manager], MACInit method [windows Media Device Manager],CSecureChannelClient interface, scclient/CSecureChannelClient::MACInit, wmdm.csecurechannelclient_macinit
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: TS_SB_SORT_BY
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
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: ADAM
---

# CSecureChannelClient::MACInit


## -description



The <b>MACInit</b> method acquires a message authentication code (MAC) channel.




## -parameters




### -param phMAC [out]

Pointer to the MAC handle for the parameter data. The handle is acquired by <b>MACInit</b> to be used for subsequent <a href="https://msdn.microsoft.com/b868d422-535d-44f5-9713-bfa049da8a4e">MACUpdate</a> and <a href="https://msdn.microsoft.com/64dc8e36-c135-415f-a646-04919e4d031d">MACFinal</a> calls. This datatype is declared in Sac.h installed with the Windows Media Format SDK.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn938542">Error Codes</a>.

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



<b>MACInit</b> begins a message authentication code (MAC) session. For example, <b>MACInit</b> should be called before content is transferred when writing to a storage device to verify the MAC returned by the <a href="https://msdn.microsoft.com/b4fb3ace-ebb5-4d95-8fce-780b5dc8e21a">IMDSPStorage::GetRights</a> call on the service provider.


#### Examples

The following example code checks the MAC received by a call to <a href="https://msdn.microsoft.com/5b654d32-b72a-44cf-a8d9-63fc0ae76171">IWMDMStorage::GetRights</a> to verify that the data has not been tampered with.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
HRESULT hr;
CSecureChannelClient *pSPClient = NULL;
hr = m_pStorage-&gt;GetRights(ppRights, pnRightsCount, abTempMAC);
if (SUCCEEDED(hr))
{
    // Verify MAC returned by GetRights on the service provider.
    pSPClient-&gt;MACInit(&amp;hMAC);
    pSPClient-&gt;MACUpdate(hMAC, (BYTE*)(*ppRights),
                       sizeof(WMDMRIGHTS) * (*pnRightsCount));
    pSPClient-&gt;MACUpdate(hMAC, (BYTE*)(pnRightsCount),
                        sizeof(*pnRightsCount));
    pSPClient-&gt;MACFinal(hMAC, abMACVerify);
    if (memcmp(abMACVerify, abTempMAC, WMDM_MAC_LENGTH) != 0)
    {
        hr = WMDM_E_MAC_CHECK_FAILED;
        goto exit;
    }
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/f02220b8-0d1c-416c-97ea-e5e7455fcbba">CSecureChannelClient Class</a>



<a href="https://msdn.microsoft.com/64dc8e36-c135-415f-a646-04919e4d031d">CSecureChannelClient::MACFinal</a>



<a href="https://msdn.microsoft.com/b868d422-535d-44f5-9713-bfa049da8a4e">CSecureChannelClient::MACUpdate</a>



<a href="https://msdn.microsoft.com/6cb49f6b-e303-4840-9343-9891e75e07a4">Message Authentication</a>
 

 

