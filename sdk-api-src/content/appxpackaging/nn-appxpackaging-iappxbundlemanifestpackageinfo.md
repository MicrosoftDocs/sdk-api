---
UID: NN:appxpackaging.IAppxBundleManifestPackageInfo
title: IAppxBundleManifestPackageInfo
author: windows-driver-content
description: Provides a read-only object model for a &lt;Package&gt; element in a bundle package manifest.
old-location: appxpkg\iappxbundlemanifestpackageinfo.htm
old-project: appxpkg
ms.assetid: B9272875-E02A-4443-82B3-C64104E8291C
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IAppxBundleManifestPackageInfo, IAppxBundleManifestPackageInfo interface [App packaging and management], IAppxBundleManifestPackageInfo interface [App packaging and management],described, appxpackaging/IAppxBundleManifestPackageInfo, appxpkg.iappxbundlemanifestpackageinfo
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
req.typenames: APPX_PACKAGE_EDITOR_UPDATE_PACKAGE_OPTION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	AppxPackaging.h
api_name:
-	IAppxBundleManifestPackageInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxBundleManifestPackageInfo interface


## -description


Provides a read-only object model for a &lt;Package&gt; element in a bundle package manifest. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppxBundleManifestPackageInfo</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAppxBundleManifestPackageInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAppxBundleManifestPackageInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926842">GetFileName</a>
</td>
<td align="left" width="63%">
Retrieves the file-name attribute of the package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff548008">GetOffset</a>
</td>
<td align="left" width="63%">
Retrieves the offset of the package relative to the beginning of the bundle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5C7F52C3-AB72-4023-900B-53E3B5504213">GetPackageId</a>
</td>
<td align="left" width="63%">
Retrieves an object that represents the identity of the app package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/965E48E3-7C60-4299-85F4-07CB879E7B39">GetPackageType</a>
</td>
<td align="left" width="63%">
Retrieves the type of package that is represented by the package info.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451131">GetResources</a>
</td>
<td align="left" width="63%">
Retrieves an enumerator that iterates through all the &lt;Resource&gt; elements that are defined in the app package's manifest.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/BA9BB378-D9AF-4D96-88B0-219A5545397A">GetSize</a>
</td>
<td align="left" width="63%">
Retrieves the size of the package, in bytes.

</td>
</tr>
</table> 

