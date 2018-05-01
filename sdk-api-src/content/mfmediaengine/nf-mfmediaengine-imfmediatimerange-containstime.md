---
UID: NF:mfmediaengine.IMFMediaTimeRange.ContainsTime
title: IMFMediaTimeRange::ContainsTime method
author: windows-driver-content
description: Queries whether a specified time falls within any of the time ranges.
old-location: mf\imfmediatimerange_containstime.htm
old-project: medfound
ms.assetid: 67BA2464-D8F0-4A5C-9C12-DBD9AD0238A7
ms.author: windowsdriverdev
ms.date: 4/23/2018
ms.keywords: ContainsTime method [Media Foundation], ContainsTime method [Media Foundation], IMFMediaTimeRange interface, ContainsTime,IMFMediaTimeRange.ContainsTime, IMFMediaTimeRange, IMFMediaTimeRange interface [Media Foundation], ContainsTime method, IMFMediaTimeRange::ContainsTime, mf.imfmediatimerange_containstime, mfmediaengine/IMFMediaTimeRange::ContainsTime
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: MF_TIMED_TEXT_WRITING_MODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfmediaengine.h
api_name:
-	IMFMediaTimeRange.ContainsTime
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFMediaTimeRange::ContainsTime method


## -description


Queries whether a specified time falls within any of the time ranges.


## -parameters




### -param time [in]

The time, in seconds.


## -returns



Returns <b>TRUE</b> if any time range contained in this object spans the value of the <i>time</i> parameter. Otherwise, returns <b>FALSE</b>.




## -remarks



This method returns <b>TRUE</b> if the following condition holds for any time range in the list:

<i>start</i>
<i>time</i>
<i>time</i>
<i>end</i>



## -see-also




<a href="https://msdn.microsoft.com/E39646E6-66F4-4413-A84B-43039689AEE7">IMFMediaTimeRange</a>
 

 

