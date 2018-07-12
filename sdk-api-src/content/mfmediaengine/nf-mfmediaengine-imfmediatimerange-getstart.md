---
UID: NF:mfmediaengine.IMFMediaTimeRange.GetStart
title: IMFMediaTimeRange::GetStart
author: windows-sdk-content
description: Gets the start time for a specified time range.
old-location: mf\imfmediatimerange_getstart.htm
old-project: medfound
ms.assetid: E02CFE99-78B8-4923-8922-467A55442802
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: GetStart, GetStart method [Media Foundation], GetStart method [Media Foundation],IMFMediaTimeRange interface, IMFMediaTimeRange interface [Media Foundation],GetStart method, IMFMediaTimeRange.GetStart, IMFMediaTimeRange::GetStart, mf.imfmediatimerange_getstart, mfmediaengine/IMFMediaTimeRange::GetStart
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MF_MEDIA_ENGINE_KEYERR
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfmediaengine.h
api_name:
 - IMFMediaTimeRange.GetStart
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFMediaTimeRange::GetStart


## -description


Gets the start time for a specified time range.


## -parameters




### -param index [in]

The zero-based index of the time range to query. To get the  number of time ranges, call <a href="https://msdn.microsoft.com/0865A667-A09E-4F42-A420-4A155AD34394">IMFMediaTimeRange::GetLength</a>.


### -param pStart [out]

Receives the start time, in seconds.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method corresponds to the <b>TimeRanges.start</b> method in HTML5.




## -see-also




<a href="https://msdn.microsoft.com/E39646E6-66F4-4413-A84B-43039689AEE7">IMFMediaTimeRange</a>
 

 

