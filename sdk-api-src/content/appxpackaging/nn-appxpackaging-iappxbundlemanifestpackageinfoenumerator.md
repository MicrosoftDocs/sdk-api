---
UID: NN:appxpackaging.IAppxBundleManifestPackageInfoEnumerator
title: IAppxBundleManifestPackageInfoEnumerator
author: windows-sdk-content
description: Provides a read-only object model for the list of payload packages that are described in a bundle package manifest.
old-location: appxpkg\iappxbundlemanifestpackageinfoenumerator.htm
tech.root: appxpkg
ms.assetid: 4861D5CF-9FDC-4BAA-8462-D239DAEB5195
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: IAppxBundleManifestPackageInfoEnumerator, IAppxBundleManifestPackageInfoEnumerator interface [App packaging and management], IAppxBundleManifestPackageInfoEnumerator interface [App packaging and management],described, appxpackaging/IAppxBundleManifestPackageInfoEnumerator, appxpkg.iappxbundlemanifestpackageinfoenumerator
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: appxpackaging.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
 - IAppxBundleManifestPackageInfoEnumerator
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAppxBundleManifestPackageInfoEnumerator interface


## -description


Provides a read-only object model for the list of payload packages that are described in a bundle package manifest. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppxBundleManifestPackageInfoEnumerator</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAppxBundleManifestPackageInfoEnumerator</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAppxBundleManifestPackageInfoEnumerator</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/52F525CB-162B-47E9-BF85-B920CBCCD983">GetCurrent</a>
</td>
<td align="left" width="63%">
Gets the &lt;Package&gt; element at the current position of the enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ED12F498-1F8D-45B2-9CFE-7215D2D87C3F">GetHasCurrent</a>
</td>
<td align="left" width="63%">
Determines whether there are more elements in the enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8818FC6B-28CB-420F-A5BB-BCB62DFD4A78">MoveNext</a>
</td>
<td align="left" width="63%">
Advances the position of the enumerator to the next &lt;Package&gt; element.

</td>
</tr>
</table> 

