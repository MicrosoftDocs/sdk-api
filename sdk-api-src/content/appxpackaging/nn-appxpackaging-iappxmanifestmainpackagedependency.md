---
UID: NN:appxpackaging.IAppxManifestMainPackageDependency
title: IAppxManifestMainPackageDependency
author: windows-sdk-content
description: Provides access to attribute values of the main package dependency.
old-location: appxpkg\iappxmanifestmainpackagedependency.htm
old-project: appxpkg
ms.assetid: E9B04DAD-BD45-4699-9EB1-99CF59F8D934
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: IAppxManifestMainPackageDependency, IAppxManifestMainPackageDependency interface [App packaging and management], IAppxManifestMainPackageDependency interface [App packaging and management],described, appxpackaging/IAppxManifestMainPackageDependency, appxpkg.iappxmanifestmainpackagedependency
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
 - IAppxManifestMainPackageDependency
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxManifestMainPackageDependency interface


## -description


Provides access to attribute values of the main package dependency.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppxManifestMainPackageDependency</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAppxManifestMainPackageDependency</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAppxManifestMainPackageDependency</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0D891C01-F149-4BF0-99E7-E2AAD6D781AD">GetName</a>
</td>
<td align="left" width="63%">
Gets the name of the main package dependency from the AppxManifest.xml.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4F8E3E60-CE14-48C1-8367-10AA293F72F6">GetPackageFamilyName</a>
</td>
<td align="left" width="63%">
Gets the package family name of the main package dependency from the AppxManifest.xml.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4E7AD93A-27B6-4FE0-8803-EF1ACCB82986">GetPublisher</a>
</td>
<td align="left" width="63%">
Gets the publisher of the main package dependency from the AppxManifest.xml.

</td>
</tr>
</table> 

