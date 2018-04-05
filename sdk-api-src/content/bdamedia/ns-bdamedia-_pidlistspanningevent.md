---
UID: NS:bdamedia._PIDListSpanningEvent
title: "_PIDListSpanningEvent"
author: windows-driver-content
description: Contains a list of packet identifiers (PIDs).
old-location: mstv\pidlistspanningevent.htm
old-project: mstv
ms.assetid: 7c2a8e24-0919-4fe6-9a31-a1d4b1d119ed
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: PIDListSpanningEvent, PIDListSpanningEvent structure [Microsoft TV Technologies], _PIDListSpanningEvent, bdamedia/PIDListSpanningEvent, mstv.pidlistspanningevent
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: bdamedia.h
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
req.typenames: PIDListSpanningEvent
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	bdamedia.h
api_name:
-	PIDListSpanningEvent
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _PIDListSpanningEvent structure


## -description


Contains a list of packet identifiers (PIDs).


## -struct-fields




### -field wPIDCount

The number of elements in the <b>pulPIDs</b> array.


### -field pulPIDs

An array of PIDs. The array might be larger than the size given in the structure declaration. Use the value of <b>wPIDCount</b> to determine the size.

