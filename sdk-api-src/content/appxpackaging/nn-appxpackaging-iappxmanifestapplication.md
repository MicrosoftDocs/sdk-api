---
UID: NN:appxpackaging.IAppxManifestApplication
title: IAppxManifestApplication
author: windows-driver-content
description: Provides access to attribute values of the application.
old-location: appxpkg\iappxmanifestapplication.htm
old-project: appxpkg
ms.assetid: 16FC78D1-7387-4C90-9F63-BCFA110BC487
ms.author: windowsdriverdev
ms.date: 3/30/2018
ms.keywords: IAppxManifestApplication, IAppxManifestApplication interface [App packaging and management], IAppxManifestApplication interface [App packaging and management], described, appxpackaging/IAppxManifestApplication, appxpkg.iappxmanifestapplication
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
req.typenames: APPX_PACKAGE_ARCHITECTURE2
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	AppxPackaging.h
api_name:
-	IAppxManifestApplication
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxManifestApplication interface


## -description


Provides access to attribute values of the application.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppxManifestApplication</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAppxManifestApplication</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAppxManifestApplication</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/A1CD62B4-A314-43B3-AD80-3EB3EDF63B3D">GetAppUserModelId</a>
</td>
<td align="left" width="63%">
Gets the application user model identifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff597621">GetStringValue</a>
</td>
<td align="left" width="63%">
Gets the value of a string element in the application metadata section of the manifest.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/49955DE0-A6BE-4FD7-B8E3-E4126B3C4B8F">IAppxManifestApplicationsEnumerator</a>



<a href="https://msdn.microsoft.com/3DA45F2F-7088-4A9B-968C-91E402CAA412">IAppxManifestReader</a>
 

 

