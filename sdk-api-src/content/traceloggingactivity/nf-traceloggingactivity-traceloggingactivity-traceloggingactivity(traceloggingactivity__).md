---
UID: NF:traceloggingactivity.TraceLoggingActivity.TraceLoggingActivity(TraceLoggingActivity &&)
title: TraceLoggingActivity::TraceLoggingActivity(TraceLoggingActivity &&) (traceloggingactivity.h)
description: Creates a new TraceLoggingActivity object.
old-location: tracelogging\traceloggingactivity_traceloggingactivity.htm
tech.root: tracelogging
ms.assetid: 21A4BB42-1D78-48A9-A037-64A3508A9957
ms.date: 12/05/2018
ms.keywords: TraceLoggingActivity, TraceLoggingActivity interface,TraceLoggingActivity method, TraceLoggingActivity method, TraceLoggingActivity method,TraceLoggingActivity interface, TraceLoggingActivity.TraceLoggingActivity, TraceLoggingActivity.TraceLoggingActivity(TraceLoggingActivity &&), TraceLoggingActivity::TraceLoggingActivity, TraceLoggingActivity::TraceLoggingActivity(TraceLoggingActivity &&), tracelogging.traceloggingactivity_traceloggingactivity, traceloggingactivity/TraceLoggingActivity::TraceLoggingActivity
f1_keywords:
- traceloggingactivity/TraceLoggingActivity.TraceLoggingActivity
dev_langs:
- c++
req.header: traceloggingactivity.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2012 R2
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
- traceloggingactivity.h
api_name:
- TraceLoggingActivity.TraceLoggingActivity
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# TraceLoggingActivity::TraceLoggingActivity(TraceLoggingActivity &&)


## -description


Creates a new <a href="https://docs.microsoft.com/windows/desktop/api/traceloggingactivity/nl-traceloggingactivity-traceloggingactivity~r1">TraceLoggingActivity</a> object.

<b>TraceLoggingActivity</b> is a class template.


## -parameters




### -param rhs

A reference to a <b>TraceLoggingActivity</b>.




## -returns



This method does not return a value.




## -remarks



<div class="alert"><b>Note</b>  <p class="note"><b>TraceLoggingActivity</b> is a class template.

<p class="note">Default template values are: 

<p class="note"> TraceLoggingHProvider _HProvider = const&amp; provider 

<p class="note">UINT64 _Keyword = 0 

<p class="note"> UINT8 _Level = WINEVENT_LEVEL_VERBOSE

<p class="note">typename TlgReflectorTag = _TlgReflectorTag_Param0IsHProvider

</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/traceloggingactivity/nl-traceloggingactivity-traceloggingactivity~r1">TraceLoggingActivity</a>
 

 

