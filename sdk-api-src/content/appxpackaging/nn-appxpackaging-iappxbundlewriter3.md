---
UID: NN:appxpackaging.IAppxBundleWriter3
title: IAppxBundleWriter3
author: windows-sdk-content
description: Provides a write-only object model for bundle packages.
old-location: appxpkg\iappxbundlewriter3.htm
old-project: appxpkg
ms.assetid: 2596E2DA-D9B6-4BBE-AC05-5CE253CE6DDC
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: IAppxBundleWriter3, IAppxBundleWriter3 interface [App packaging and management], IAppxBundleWriter3 interface [App packaging and management],described, appxpackaging/IAppxBundleWriter3, appxpkg.iappxbundlewriter3
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: appxpackaging.h
req.include-header: 
req.redist: 
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - AppxPackaging.h
api_name:
 - IAppxBundleWriter3
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxBundleWriter3 interface


## -description


Provides a write-only object model for bundle packages.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppxBundleWriter3</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAppxBundleWriter3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAppxBundleWriter3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/99969971-9153-47C9-AF9C-7BF1D56EC54D">AddPackageReference</a>
</td>
<td align="left" width="63%">
Adds a reference to an optional app package or a payload file within an app bundle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7AD526CD-9FF2-4A2A-BD12-21A0A9E1BA6E">Close</a>
</td>
<td align="left" width="63%">
Finalizes the bundle package by writing footprint files at the end of the package, and closes the writer’s output stream.

</td>
</tr>
</table> 

