---
UID: NN:appxpackaging.IAppxManifestMainPackageDependenciesEnumerator
title: IAppxManifestMainPackageDependenciesEnumerator
author: windows-sdk-content
description: Enumerates &lt;MainPackageDependency&gt; elements from an app manifest.
old-location: appxpkg\iappxmanifestmainpackagedependenciesenumerator.htm
old-project: appxpkg
ms.assetid: EB511040-5011-4B79-AFEE-DFF42E11025B
ms.author: windowssdkdev
ms.date: 04/26/2018
ms.keywords: IAppxManifestMainPackageDependenciesEnumerator, IAppxManifestMainPackageDependenciesEnumerator interface [App packaging and management], IAppxManifestMainPackageDependenciesEnumerator interface [App packaging and management],described, appxpackaging/IAppxManifestMainPackageDependenciesEnumerator, appxpkg.iappxmanifestmainpackagedependenciesenumerator
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: appxpackaging.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: AppxPackaging.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: APPX_PACKAGE_EDITOR_UPDATE_PACKAGE_OPTION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	AppxPackaging.h
api_name:
-	IAppxManifestMainPackageDependenciesEnumerator
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxManifestMainPackageDependenciesEnumerator interface


## -description


Enumerates &lt;MainPackageDependency&gt; elements from an app manifest.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppxManifestMainPackageDependenciesEnumerator</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAppxManifestMainPackageDependenciesEnumerator</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAppxManifestMainPackageDependenciesEnumerator</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/14C7F3F9-38FE-4FC2-9255-0A728A1488C0">GetCurrent</a>
</td>
<td align="left" width="63%">
Gets the &lt;MainPackageDependency&gt; element at the current position of the enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/DB350E8E-8A0B-4742-B7E3-2133603A0714">GetHasCurrent</a>
</td>
<td align="left" width="63%">
Determines whether there is a &lt;MainPackageDependency&gt; element at the current position of the enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C9E34671-5B56-4A6D-B728-C074F9BDB6D6">MoveNext</a>
</td>
<td align="left" width="63%">
Advances the position of the enumerator to the next &lt;MainPackageDependency&gt; element.

</td>
</tr>
</table> 

