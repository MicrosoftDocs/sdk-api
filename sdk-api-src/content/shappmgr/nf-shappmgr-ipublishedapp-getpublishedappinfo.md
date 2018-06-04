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

# IPublishedApp::GetPublishedAppInfo


## -description



		Gets publishing-related information about an application published by an application publisher.
		


## -parameters




### -param ppai






#### - pInfo [out]

Type: <b><a href="https://msdn.microsoft.com/927c58d3-4208-4fd3-a3fa-18ae7d8d3136">PUBAPPINFO</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/927c58d3-4208-4fd3-a3fa-18ae7d8d3136">PUBAPPINFO</a> structure that returns the application information.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The dwMask member of the <a href="https://msdn.microsoft.com/927c58d3-4208-4fd3-a3fa-18ae7d8d3136">PUBAPPINFO</a> structure indicates which members have been requested. Note that Add/Remove Programs will not set the PAI_SCHEDULEDTIME and PAI_EXPIREDTIME bits.  However, the corresponding values stScheduled and stExpired will be used when applicable if the implementation provides them.  A publisher should provide this data if it is available.


#### Examples

The example shows a sample implementation:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT CPubApp::GetPublishedAppInfo(PUBAPPINFO *pInfo)
{
    if (sizeof(PUBAPPINFO) != pInfo-&gt;cbSize)
        return E_FAIL;
		
    // Add/Remove Programs will use these items but will not ask for them.

    pInfo-&gt;dwMask |= (PAI_EXPIRETIME | PAI_SCHEDULEDTIME);

    // First save off the mask of requested data items.

    const DWORD dwMask = pInfo-&gt;dwMask;

    // Zero-out the mask.  The bits should be set as items are retrieved.

    pInfo-&gt;dwMask = 0;

    // Call an internal function that obtains data and sets
    // bits in pInfo-&gt;dwMask for each item obtained.

    return get_pub_app_info(pInfo, dwMask);
}


					</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/5391444a-53b6-48c9-9a94-d045b3f97182">IAppPublisher</a>



<a href="https://msdn.microsoft.com/89a06b1d-1b72-46ca-91cd-bb63ea0cbff7">IEnumPublishedApps</a>



<a href="https://msdn.microsoft.com/a5a44e74-494a-4c9b-8bf3-85c6093b2c0e">IPublishedApp</a>



<a href="https://msdn.microsoft.com/927c58d3-4208-4fd3-a3fa-18ae7d8d3136">PUBAPPINFO</a>
 

 

