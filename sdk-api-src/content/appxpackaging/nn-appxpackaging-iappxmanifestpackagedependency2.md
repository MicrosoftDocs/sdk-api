---
UID: NN:appxpackaging.IAppxManifestPackageDependency2
title: IAppxManifestPackageDependency2
author: windows-driver-content
description: Describes the dependency of one package on another package.
old-location: appxpkg\iappxmanifestpackagedependency2.htm
old-project: appxpkg
ms.assetid: 9363C5BB-BDEF-4671-9545-5B8C0EF14FBE
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IAppxManifestPackageDependency2, IAppxManifestPackageDependency2 interface [App packaging and management], IAppxManifestPackageDependency2 interface [App packaging and management], described, appxpackaging/IAppxManifestPackageDependency2, appxpkg.iappxmanifestpackagedependency2
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	IAppxManifestPackageDependency2
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxManifestPackageDependency2 interface


## -description


Describes the dependency of one package on another package.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppxManifestPackageDependency2</b> interface inherits from <a href="https://msdn.microsoft.com/1A5515DA-4A9E-40EE-9AAC-F267DAE9DDBA">IAppxManifestPackageDependency</a>. <b>IAppxManifestPackageDependency2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAppxManifestPackageDependency2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/BB83C97E-9E89-440C-8A14-88062F1394CF">GetMaxMajorVersionTested</a>
</td>
<td align="left" width="63%">
Returns the maximum major version number of  the package that is tested to be compatible
with the current package.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/1A5515DA-4A9E-40EE-9AAC-F267DAE9DDBA">IAppxManifestPackageDependency</a>
 

 

