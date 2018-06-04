---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# CSecureChannelClient::MACUpdate


## -description



The <b>MACUpdate</b> method adds a value to a message authentication code (MAC).




## -parameters




### -param hMAC [in]

Handle to the array specifying the MAC for the current parameter data. This handle is returned from the <a href="https://msdn.microsoft.com/d383d040-55f7-4ed7-b5b8-8e963b6cb16a">MACInit</a> method. This datatype is declared in Sac.h installed with the Windows Media Format SDK.


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
<td>A parameter is invalid or is a <b>NULL</b> pointer.</td>
</tr>
<tr>
<td>E_FAIL</td>
<td>An unspecified error occurred.</td>
</tr>
</table>
 




## -remarks



An application calls <b>MACUpdate</b> repeatedly with each piece of data to add to the MAC. <b>MACInit</b> must always be called before <b>MACUpdate</b>, and <a href="https://msdn.microsoft.com/64dc8e36-c135-415f-a646-04919e4d031d">MACFinal</a> must always be called after <b>MACUpdate</b>. <b>MACInit</b> acquires the MAC handle, <b>phMAC</b>, to be used by the <b>MACUpdate</b> and <b>MACFinal</b> methods.


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



<a href="https://msdn.microsoft.com/6cb49f6b-e303-4840-9343-9891e75e07a4">Message Authentication</a>
 

 

