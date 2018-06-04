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

# IAppxManifestResourcesEnumerator interface


## -description


Enumerates the resources defined in the package manifest.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppxManifestResourcesEnumerator</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAppxManifestResourcesEnumerator</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAppxManifestResourcesEnumerator</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/FCFEEC2B-F047-4417-B110-BD3C90C30BE2">GetCurrent</a>
</td>
<td align="left" width="63%">
Gets the resource at the current position of the enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/72798FDF-3296-4AC7-9BA0-212457F9BEC7">GetHasCurrent</a>
</td>
<td align="left" width="63%">
Determines whether there is a resource at the current position of the enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/CD5A7FF9-A28E-4857-AE7B-92F8EEBA0235">MoveNext</a>
</td>
<td align="left" width="63%">
Advances the position of the enumerator to the next resource.

</td>
</tr>
</table> 


## -remarks



This object can be retrieved by using the <a href="https://msdn.microsoft.com/library/windows/hardware/hh451131">GetResources</a> method of a  <a href="https://msdn.microsoft.com/3DA45F2F-7088-4A9B-968C-91E402CAA412">IAppxManifestReader</a> or <a href="https://msdn.microsoft.com/B10A1ACB-12F4-4338-A6D6-6D2B829F9D62">IAppxManifestReader2</a> object. But, starting with Windows 8.1, use <b>IAppxManifestReader2::GetResources</b> because it iterates over more resource qualifiers, such as, <b>Scale</b> and <b>DXFeatureLevel</b>. 




## -see-also




<a href="https://msdn.microsoft.com/3DA45F2F-7088-4A9B-968C-91E402CAA412">IAppxManifestReader</a>



<a href="https://msdn.microsoft.com/B10A1ACB-12F4-4338-A6D6-6D2B829F9D62">IAppxManifestReader2</a>



<a href="https://msdn.microsoft.com/2F0109C2-99F5-4AEE-9596-153764FA8FA3">IAppxManifestReader::GetResources</a>
 

 

