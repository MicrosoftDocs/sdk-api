---
UID: NN:appxpackaging.IAppxBundleWriter4
title: IAppxBundleWriter4
author: windows-sdk-content
description: Provides a write-only object model for bundle packages.
old-location: appxpkg\iappxbundlewriter4.htm
tech.root: appxpkg
ms.assetid: 9BB81F38-8451-4D3B-B0B6-31AF3001AB17
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IAppxBundleWriter4, IAppxBundleWriter4 interface [App packaging and management], IAppxBundleWriter4 interface [App packaging and management],described, appxpackaging/IAppxBundleWriter4, appxpkg.iappxbundlewriter4
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IAppxBundleWriter4
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAppxBundleWriter4 interface


## -description


Provides a write-only object model for bundle packages.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppxBundleWriter4</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAppxBundleWriter4</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAppxBundleWriter4</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2C655FF8-93F5-4132-8D61-1C47DB317043">AddExternalPackageReference</a>
</td>
<td align="left" width="63%">
Adds a reference within the package bundle to an external app package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/16ADE271-C507-4CC4-BB42-E76438B79436">AddPackageReference</a>
</td>
<td align="left" width="63%">
Adds a reference to an optional app package or a payload file within an app bundle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5D313F6C-F2EC-42A4-A4A8-8026E7DBF67B">AddPayloadPackage</a>
</td>
<td align="left" width="63%">
Adds a new app package to the bundle.

</td>
</tr>
</table> 

