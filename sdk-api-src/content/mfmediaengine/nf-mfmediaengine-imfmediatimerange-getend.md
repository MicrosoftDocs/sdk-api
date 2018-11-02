---
UID: NF:mfmediaengine.IMFMediaTimeRange.GetEnd
title: IMFMediaTimeRange::GetEnd
author: windows-sdk-content
description: Gets the end time for a specified time range.
old-location: mf\imfmediatimerange_getend.htm
tech.root: medfound
ms.assetid: 864C0DEE-A1F7-488C-9A9D-366602667DE9
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: GetEnd, GetEnd method [Media Foundation], GetEnd method [Media Foundation],IMFMediaTimeRange interface, IMFMediaTimeRange interface [Media Foundation],GetEnd method, IMFMediaTimeRange.GetEnd, IMFMediaTimeRange::GetEnd, mf.imfmediatimerange_getend, mfmediaengine/IMFMediaTimeRange::GetEnd
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - mfmediaengine.h
api_name:
 - IMFMediaTimeRange.GetEnd
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFMediaTimeRange::GetEnd


## -description


Gets the end time for a specified time range.


## -parameters




### -param index [in]

The zero-based index of the time range to query. To get the  number of time ranges, call <a href="https://msdn.microsoft.com/0865A667-A09E-4F42-A420-4A155AD34394">IMFMediaTimeRange::GetLength</a>.


### -param pEnd [out]

Receives the end time, in seconds.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method corresponds to the <b>TimeRanges.end</b> method in HTML5.




## -see-also




<a href="https://msdn.microsoft.com/E39646E6-66F4-4413-A84B-43039689AEE7">IMFMediaTimeRange</a>
 

 

