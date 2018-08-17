---
UID: NN:appxpackaging.IAppxManifestPackageId2
title: IAppxManifestPackageId2
author: windows-sdk-content
description: Provides access to the app package identity.
old-location: appxpkg\iappxmanifestpackageid2.htm
old-project: appxpkg
ms.assetid: 27344514-B9B9-46EC-9A44-577C0C9361C8
ms.author: windowssdkdev
ms.date: 08/15/2018
ms.keywords: IAppxManifestPackageId2, IAppxManifestPackageId2 interface [App packaging and management], IAppxManifestPackageId2 interface [App packaging and management],described, appxpackaging/IAppxManifestPackageId2, appxpkg.iappxmanifestpackageid2
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
 - IAppxManifestPackageId2
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxManifestPackageId2 interface


## -description


Provides access to the app package identity.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppxManifestPackageId2</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAppxManifestPackageId2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAppxManifestPackageId2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/FBC34FBA-C6BB-45AD-8005-5C2B91A1369D">GetArchitecture2</a>
</td>
<td align="left" width="63%">
Gets the processor architecture as defined in the manifest.

</td>
</tr>
</table> 


## -remarks



Package identity information is specified using the <b>Identity</b> element in the package manifest.

This object can be retrieved using the <a href="https://msdn.microsoft.com/67E1B1A4-E934-4CCF-AF94-A7923B192A21">IAppxManifestReader::GetPackageId</a> method.



