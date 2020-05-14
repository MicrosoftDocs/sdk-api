---
UID: NF:mfmediaengine.IMFMediaTimeRange.ContainsTime
title: IMFMediaTimeRange::ContainsTime (mfmediaengine.h)
description: Queries whether a specified time falls within any of the time ranges.helpviewer_keywords: ["ContainsTime","ContainsTime method [Media Foundation]","ContainsTime method [Media Foundation]","IMFMediaTimeRange interface","IMFMediaTimeRange interface [Media Foundation]","ContainsTime method","IMFMediaTimeRange.ContainsTime","IMFMediaTimeRange::ContainsTime","mf.imfmediatimerange_containstime","mfmediaengine/IMFMediaTimeRange::ContainsTime"]
old-location: mf\imfmediatimerange_containstime.htm
tech.root: medfound
ms.assetid: 67BA2464-D8F0-4A5C-9C12-DBD9AD0238A7
ms.date: 12/05/2018
ms.keywords: ContainsTime, ContainsTime method [Media Foundation], ContainsTime method [Media Foundation],IMFMediaTimeRange interface, IMFMediaTimeRange interface [Media Foundation],ContainsTime method, IMFMediaTimeRange.ContainsTime, IMFMediaTimeRange::ContainsTime, mf.imfmediatimerange_containstime, mfmediaengine/IMFMediaTimeRange::ContainsTime
f1_keywords:
- mfmediaengine/IMFMediaTimeRange.ContainsTime
dev_langs:
- c++
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
- IMFMediaTimeRange.ContainsTime
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFMediaTimeRange::ContainsTime


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




<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediatimerange">IMFMediaTimeRange</a>
 

 

