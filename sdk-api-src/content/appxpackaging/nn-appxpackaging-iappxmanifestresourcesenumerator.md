---
UID: NN:appxpackaging.IAppxManifestResourcesEnumerator
title: IAppxManifestResourcesEnumerator
author: windows-sdk-content
description: Enumerates the resources defined in the package manifest.
old-location: appxpkg\iappxmanifestresourcesenumerator.htm
tech.root: appxpkg
ms.assetid: D76C7512-962F-4AFE-934F-BBC215B5FE99
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IAppxManifestResourcesEnumerator, IAppxManifestResourcesEnumerator interface [App packaging and management], IAppxManifestResourcesEnumerator interface [App packaging and management],described, appxpackaging/IAppxManifestResourcesEnumerator, appxpkg.iappxmanifestresourcesenumerator
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: appxpackaging.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: AppxPackaging.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - AppxPackaging.h
api_name:
 - IAppxManifestResourcesEnumerator
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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



This object can be retrieved by using the <a href="https://msdn.microsoft.com/2F0109C2-99F5-4AEE-9596-153764FA8FA3">GetResources</a> method of a  <a href="https://msdn.microsoft.com/3DA45F2F-7088-4A9B-968C-91E402CAA412">IAppxManifestReader</a> or <a href="https://msdn.microsoft.com/B10A1ACB-12F4-4338-A6D6-6D2B829F9D62">IAppxManifestReader2</a> object. But, starting with Windows 8.1, use <b>IAppxManifestReader2::GetResources</b> because it iterates over more resource qualifiers, such as, <b>Scale</b> and <b>DXFeatureLevel</b>. 




## -see-also




<a href="https://msdn.microsoft.com/3DA45F2F-7088-4A9B-968C-91E402CAA412">IAppxManifestReader</a>



<a href="https://msdn.microsoft.com/B10A1ACB-12F4-4338-A6D6-6D2B829F9D62">IAppxManifestReader2</a>



<a href="https://msdn.microsoft.com/2F0109C2-99F5-4AEE-9596-153764FA8FA3">IAppxManifestReader::GetResources</a>
 

 

