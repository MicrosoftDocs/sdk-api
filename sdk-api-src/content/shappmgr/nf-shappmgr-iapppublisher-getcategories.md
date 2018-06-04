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

# IAppPublisher::GetCategories


## -description


Retrieves a structure listing the categories provided by an application publisher.


## -parameters




### -param pAppCategoryList






#### - pInfoList [out]

Type: <b><a href="https://msdn.microsoft.com/c590d9ab-ab41-4192-a6c2-c6c2c931e873">APPCATEGORYINFOLIST</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/c590d9ab-ab41-4192-a6c2-c6c2c931e873">APPCATEGORYINFOLIST</a> structure. This structure's <b>cCategory</b> member returns the count of supported categories. The <b>pCategoryInfo</b> member returns a pointer to an array of <a href="https://msdn.microsoft.com/7a0e61cb-97f8-4ca2-a85a-889e671099d0">APPCATEGORYINFO</a> structures. This array contains all the categories an application publisher supports and must be allocated using <a href="https://msdn.microsoft.com/c4cb588d-9482-4f90-a92e-75b604540d5c">CoTaskMemAlloc</a> and freed using <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The Add/Remove Programs Control Panel Application passes the ID returned for a category to the <a href="https://msdn.microsoft.com/b24c3007-662a-4c42-9ca7-367180152deb">IAppPublisher::EnumApps</a> method to identify which category is to be enumerated.


#### Examples

The following example shows how to calculate the size of the array of <a href="https://msdn.microsoft.com/7a0e61cb-97f8-4ca2-a85a-889e671099d0">APPCATEGORYINFO</a> structures that is returned by <b>IAppPublisher::GetCategories</b>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>size_t CategoryListArraySize = sizeof(APPCATEGORYINFO) * pInfoList-&gt;cCategory;</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/7a0e61cb-97f8-4ca2-a85a-889e671099d0">APPCATEGORYINFO</a>



<a href="https://msdn.microsoft.com/c590d9ab-ab41-4192-a6c2-c6c2c931e873">APPCATEGORYINFOLIST</a>



<a href="https://msdn.microsoft.com/5391444a-53b6-48c9-9a94-d045b3f97182">IAppPublisher</a>
 

 

