---
UID: NF:appxpackaging.IAppxManifestTargetDeviceFamily.GetMaxVersionTested
title: IAppxManifestTargetDeviceFamily::GetMaxVersionTested method
author: windows-driver-content
description: Gets the maximum version tested from the AppxManifest.xml.
old-location: appxpkg\iappxmanifesttargetdevicefamily_getmaxversiontested.htm
old-project: appxpkg
ms.assetid: 65391D03-627D-4302-BE1A-6E90E3A04458
ms.author: windowsdriverdev
ms.date: 3/30/2018
ms.keywords: GetMaxVersionTested method [App packaging and management], GetMaxVersionTested method [App packaging and management], IAppxManifestTargetDeviceFamily interface, GetMaxVersionTested,IAppxManifestTargetDeviceFamily.GetMaxVersionTested, IAppxManifestTargetDeviceFamily, IAppxManifestTargetDeviceFamily interface [App packaging and management], GetMaxVersionTested method, IAppxManifestTargetDeviceFamily::GetMaxVersionTested, appxpackaging/IAppxManifestTargetDeviceFamily::GetMaxVersionTested, appxpkg.iappxmanifesttargetdevicefamily_getmaxversiontested
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: APPX_PACKAGE_ARCHITECTURE2
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	AppxPackaging.h
api_name:
-	IAppxManifestTargetDeviceFamily.GetMaxVersionTested
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxManifestTargetDeviceFamily::GetMaxVersionTested method


## -description


Gets the maximum version tested from the AppxManifest.xml.


## -parameters




### -param maxVersionTested [out, retval]

The max version tested attribute.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/52C2950B-FB7F-44A8-BAB5-BCC238B012FE">IAppxManifestTargetDeviceFamily</a>
 

 

