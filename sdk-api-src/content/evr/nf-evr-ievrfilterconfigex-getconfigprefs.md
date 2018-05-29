---
UID: NF:evr.IEVRFilterConfigEx.GetConfigPrefs
title: IEVRFilterConfigEx::GetConfigPrefs
author: windows-sdk-content
description: Gets the configuration parameters for the Microsoft DirectShow Enhanced Video Renderer Filter filter.
old-location: mf\ievrfilterconfigex_getconfigprefs.htm
old-project: medfound
ms.assetid: 8b286b77-de5f-44ce-82f4-d11a76fe2c4d
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: GetConfigPrefs, GetConfigPrefs method [Media Foundation], GetConfigPrefs method [Media Foundation],IEVRFilterConfigEx interface, IEVRFilterConfigEx interface [Media Foundation],GetConfigPrefs method, IEVRFilterConfigEx.GetConfigPrefs, IEVRFilterConfigEx::GetConfigPrefs, evr/IEVRFilterConfigEx::GetConfigPrefs, mf.ievrfilterconfigex_getconfigprefs
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
req.typenames: MFVideoMixPrefs
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	evr.h
api_name:
-	IEVRFilterConfigEx.GetConfigPrefs
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IEVRFilterConfigEx::GetConfigPrefs


## -description


Gets the configuration parameters for the Microsoft DirectShow <a href="https://msdn.microsoft.com/ead99cb3-2be2-42c6-ac22-be0c2ddf28d5">Enhanced Video Renderer Filter</a> filter.


## -parameters




### -param pdwConfigFlags [out]

Receives a  bitwise <b>OR</b> of flags from the <a href="https://msdn.microsoft.com/39d6845e-8655-4f8f-be39-76d704fd1177">EVRFilterConfigPrefs</a> enumeration.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/ead99cb3-2be2-42c6-ac22-be0c2ddf28d5">Enhanced Video Renderer Filter</a>



<a href="https://msdn.microsoft.com/bbe85dc1-af9c-4be7-9064-d61bba160942">IEVRFilterConfigEx</a>



<a href="https://msdn.microsoft.com/3617adf2-ed7b-4788-abce-58bc22a14511">Video Quality Management</a>
 

 

