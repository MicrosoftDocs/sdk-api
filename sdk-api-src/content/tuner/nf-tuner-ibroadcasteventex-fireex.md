---
UID: NF:tuner.IBroadcastEventEx.FireEx
title: IBroadcastEventEx::FireEx (tuner.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
helpviewer_keywords: ["FireEx","FireEx method [Microsoft TV Technologies]","FireEx method [Microsoft TV Technologies]","IBroadcastEventEx interface","IBroadcastEventEx interface [Microsoft TV Technologies]","FireEx method","IBroadcastEventEx.FireEx","IBroadcastEventEx::FireEx","IBroadcastEventExFireEx","mstv.ibroadcasteventex_fireex","tuner/IBroadcastEventEx::FireEx"]
old-location: mstv\ibroadcasteventex_fireex.htm
tech.root: mstv
ms.assetid: b9ad8d9d-9827-44f9-9d2b-3f662c32eb9b
ms.date: 12/05/2018
ms.keywords: FireEx, FireEx method [Microsoft TV Technologies], FireEx method [Microsoft TV Technologies],IBroadcastEventEx interface, IBroadcastEventEx interface [Microsoft TV Technologies],FireEx method, IBroadcastEventEx.FireEx, IBroadcastEventEx::FireEx, IBroadcastEventExFireEx, mstv.ibroadcasteventex_fireex, tuner/IBroadcastEventEx::FireEx
f1_keywords:
- tuner/IBroadcastEventEx.FireEx
dev_langs:
- c++
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
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
- tuner.h
api_name:
- IBroadcastEventEx.FireEx
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IBroadcastEventEx::FireEx


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
        



The <b>FireEx</b> method fires a broadcast event.


## -parameters




### -param EventID [in]

GUID that specifies the event.


### -param Param1 [in]

Specifies the first implementation-dependent parameter.


### -param Param2 [in]

Specifies the second implementation-dependent parameter.


### -param Param3 [in]

Specifies the third implementation-dependent parameter.


### -param Param4 [in]

Specifies the fourth implementation-dependent parameter.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



This method is similar to <a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-ibroadcastevent-fire">IBroadcastEvent::Fire</a>, but it includes four additional parameters for passing implementation-dependent information between the object that fires the event and the objects that wait on the event. The designer who implements the objects must determine what meaning, if any, to assign to these parameters.




## -see-also




<a href="/previous-versions/dd376295(v=vs.85)">IBroadcastEventEx Interface</a>



<a href="/previous-versions/windows/desktop/mstv/video-control-interfaces">Video Control Interfaces</a>
 

 