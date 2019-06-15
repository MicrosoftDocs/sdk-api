---
UID: NN:appxpackaging.IAppxManifestTargetDeviceFamily
title: IAppxManifestTargetDeviceFamily (appxpackaging.h)
author: windows-sdk-content
description: Retrieves information about the target device family from the AppxManifest.xml.
old-location: appxpkg\iappxmanifesttargetdevicefamily.htm
tech.root: appxpkg
ms.assetid: 52C2950B-FB7F-44A8-BAB5-BCC238B012FE
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAppxManifestTargetDeviceFamily, IAppxManifestTargetDeviceFamily interface [App packaging and management], IAppxManifestTargetDeviceFamily interface [App packaging and management],described, appxpackaging/IAppxManifestTargetDeviceFamily, appxpkg.iappxmanifesttargetdevicefamily
ms.topic: interface
f1_keywords: ["appxpackaging/IAppxManifestTargetDeviceFamily"]
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
 - IAppxManifestTargetDeviceFamily
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAppxManifestTargetDeviceFamily interface


## -description


Retrieves information about the target device family from the AppxManifest.xml.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppxManifestTargetDeviceFamily</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAppxManifestTargetDeviceFamily</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxmanifesttargetdevicefamily-getmaxversiontested">GetMaxVersionTested</a>
</td>
<td align="left" width="63%">
Gets the maximum version tested from the AppxManifest.xml.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxmanifesttargetdevicefamily-getminversion">GetMinVersion</a>
</td>
<td align="left" width="63%">
Gets the minimum version of the target device family from the AppxManifest.xml.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxmanifesttargetdevicefamily-getname">GetName</a>
</td>
<td align="left" width="63%">
Gets the name of the target device family from the AppxManifest.xml..

</td>
</tr>
</table> 

