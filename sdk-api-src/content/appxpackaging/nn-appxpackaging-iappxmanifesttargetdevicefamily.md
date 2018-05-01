---
UID: NN:appxpackaging.IAppxManifestTargetDeviceFamily
title: IAppxManifestTargetDeviceFamily
author: windows-driver-content
description: Retrieves information about the target device family from the AppxManifest.xml.
old-location: appxpkg\iappxmanifesttargetdevicefamily.htm
old-project: appxpkg
ms.assetid: 52C2950B-FB7F-44A8-BAB5-BCC238B012FE
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IAppxManifestTargetDeviceFamily, IAppxManifestTargetDeviceFamily interface [App packaging and management], IAppxManifestTargetDeviceFamily interface [App packaging and management], described, appxpackaging/IAppxManifestTargetDeviceFamily, appxpkg.iappxmanifesttargetdevicefamily
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
req.typenames: APPX_PACKAGE_EDITOR_UPDATE_PACKAGE_OPTION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	AppxPackaging.h
api_name:
-	IAppxManifestTargetDeviceFamily
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxManifestTargetDeviceFamily interface


## -description


Retrieves information about the target device family from the AppxManifest.xml.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppxManifestTargetDeviceFamily</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAppxManifestTargetDeviceFamily</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAppxManifestTargetDeviceFamily</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/65391D03-627D-4302-BE1A-6E90E3A04458">GetMaxVersionTested</a>
</td>
<td align="left" width="63%">
Gets the maximum version tested from the AppxManifest.xml.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8CE408D3-0DD7-4482-8F7E-FE731ACE58C6">GetMinVersion</a>
</td>
<td align="left" width="63%">
Gets the minimum version of the target device family from the AppxManifest.xml.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B7D3A0D3-421D-4A40-AF40-516AE51E06D4">GetName</a>
</td>
<td align="left" width="63%">
Gets the name of the target device family from the AppxManifest.xml..

</td>
</tr>
</table> 

