---
UID: NF:evr.IEVRFilterConfigEx.GetConfigPrefs
title: IEVRFilterConfigEx::GetConfigPrefs (evr.h)
description: Gets the configuration parameters for the Microsoft DirectShow Enhanced Video Renderer Filter filter.
helpviewer_keywords: ["GetConfigPrefs","GetConfigPrefs method [Media Foundation]","GetConfigPrefs method [Media Foundation]","IEVRFilterConfigEx interface","IEVRFilterConfigEx interface [Media Foundation]","GetConfigPrefs method","IEVRFilterConfigEx.GetConfigPrefs","IEVRFilterConfigEx::GetConfigPrefs","evr/IEVRFilterConfigEx::GetConfigPrefs","mf.ievrfilterconfigex_getconfigprefs"]
old-location: mf\ievrfilterconfigex_getconfigprefs.htm
tech.root: mf
ms.assetid: 8b286b77-de5f-44ce-82f4-d11a76fe2c4d
ms.date: 12/05/2018
ms.keywords: GetConfigPrefs, GetConfigPrefs method [Media Foundation], GetConfigPrefs method [Media Foundation],IEVRFilterConfigEx interface, IEVRFilterConfigEx interface [Media Foundation],GetConfigPrefs method, IEVRFilterConfigEx.GetConfigPrefs, IEVRFilterConfigEx::GetConfigPrefs, evr/IEVRFilterConfigEx::GetConfigPrefs, mf.ievrfilterconfigex_getconfigprefs
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEVRFilterConfigEx::GetConfigPrefs
 - evr/IEVRFilterConfigEx::GetConfigPrefs
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - evr.h
api_name:
 - IEVRFilterConfigEx.GetConfigPrefs
archived: true
---

# IEVRFilterConfigEx::GetConfigPrefs


## -description

Gets the configuration parameters for the Microsoft DirectShow <a href="/windows/desktop/DirectShow/enhanced-video-renderer-filter">Enhanced Video Renderer Filter</a> filter.

## -parameters

### -param pdwConfigFlags [out]

Receives a  bitwise <b>OR</b> of flags from the <a href="/windows/win32/api/evr/ne-evr-evrfilterconfigprefs">EVRFilterConfigPrefs</a> enumeration.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/DirectShow/enhanced-video-renderer-filter">Enhanced Video Renderer Filter</a>



<a href="/windows/desktop/api/evr/nn-evr-ievrfilterconfigex">IEVRFilterConfigEx</a>



<a href="/windows/desktop/medfound/video-quality-management">Video Quality Management</a>