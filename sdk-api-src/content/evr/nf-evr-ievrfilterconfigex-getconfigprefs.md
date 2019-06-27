---
UID: NF:evr.IEVRFilterConfigEx.GetConfigPrefs
title: IEVRFilterConfigEx::GetConfigPrefs (evr.h)
author: windows-sdk-content
description: Gets the configuration parameters for the Microsoft DirectShow Enhanced Video Renderer Filter filter.
old-location: mf\ievrfilterconfigex_getconfigprefs.htm
tech.root: medfound
ms.assetid: 8b286b77-de5f-44ce-82f4-d11a76fe2c4d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetConfigPrefs, GetConfigPrefs method [Media Foundation], GetConfigPrefs method [Media Foundation],IEVRFilterConfigEx interface, IEVRFilterConfigEx interface [Media Foundation],GetConfigPrefs method, IEVRFilterConfigEx.GetConfigPrefs, IEVRFilterConfigEx::GetConfigPrefs, evr/IEVRFilterConfigEx::GetConfigPrefs, mf.ievrfilterconfigex_getconfigprefs
ms.topic: method
f1_keywords: 
 - "evr/IEVRFilterConfigEx.GetConfigPrefs"
req.header: evr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - evr.h
api_name:
 - IEVRFilterConfigEx.GetConfigPrefs
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEVRFilterConfigEx::GetConfigPrefs


## -description


Gets the configuration parameters for the Microsoft DirectShow <a href="https://docs.microsoft.com/windows/desktop/DirectShow/enhanced-video-renderer-filter">Enhanced Video Renderer Filter</a> filter.


## -parameters




### -param pdwConfigFlags [out]

Receives a  bitwise <b>OR</b> of flags from the <a href="https://docs.microsoft.com/windows/desktop/api/evr/ne-evr-_evrfilterconfig_prefs">EVRFilterConfigPrefs</a> enumeration.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/enhanced-video-renderer-filter">Enhanced Video Renderer Filter</a>



<a href="https://docs.microsoft.com/windows/desktop/api/evr/nn-evr-ievrfilterconfigex">IEVRFilterConfigEx</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/video-quality-management">Video Quality Management</a>
 

 

