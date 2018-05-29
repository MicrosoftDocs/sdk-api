---
UID: NN:appxpackaging.IAppxManifestPackageDependenciesEnumerator
title: IAppxManifestPackageDependenciesEnumerator
author: windows-sdk-content
description: Enumerates the package dependencies defined in the package manifest.
old-location: appxpkg\iappxmanifestpackagedependenciesenumerator.htm
old-project: appxpkg
ms.assetid: A09709AE-301F-4457-8E02-1A88FB283A43
ms.author: windowssdkdev
ms.date: 04/26/2018
ms.keywords: IAppxManifestPackageDependenciesEnumerator, IAppxManifestPackageDependenciesEnumerator interface [App packaging and management], IAppxManifestPackageDependenciesEnumerator interface [App packaging and management],described, appxpackaging/IAppxManifestPackageDependenciesEnumerator, appxpkg.iappxmanifestpackagedependenciesenumerator
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
req.typenames: APPX_PACKAGE_EDITOR_UPDATE_PACKAGE_OPTION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	AppxPackaging.h
api_name:
-	IAppxManifestPackageDependenciesEnumerator
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxManifestPackageDependenciesEnumerator interface


## -description


Enumerates  the package dependencies defined in the package manifest.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppxManifestPackageDependenciesEnumerator</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAppxManifestPackageDependenciesEnumerator</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAppxManifestPackageDependenciesEnumerator</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/A7DDD037-2A0B-485A-AF1E-7A999780496B">GetCurrent</a>
</td>
<td align="left" width="63%">
Gets the dependency package at the current position of the enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2D06DC83-B795-47F8-A05D-4DF4E86FEDFA">GetHasCurrent</a>
</td>
<td align="left" width="63%">
Determines whether there is a package dependency at the current position of the enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/DC30BC6F-C2E2-49B4-B0A8-1973880C9B4F">MoveNext</a>
</td>
<td align="left" width="63%">
Advances the position of the enumerator to the next package dependency.

</td>
</tr>
</table> 


## -remarks



This object can be retrieved using the <a href="https://msdn.microsoft.com/C40276CC-8F97-4DCF-A5C4-193453B8FA02">IAppxManifestReader::GetPackageDependencies</a> method.




## -see-also




<a href="https://msdn.microsoft.com/1A5515DA-4A9E-40EE-9AAC-F267DAE9DDBA">IAppxManifestPackageDependency</a>
 

 

