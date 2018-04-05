---
UID: NS:bdamedia._DVBScramblingControlSpanningEvent
title: "_DVBScramblingControlSpanningEvent"
author: windows-driver-content
description: Specifies whether a DVB program stream is scrambled.
old-location: mstv\dvbscramblingcontrolspanningevent.htm
old-project: mstv
ms.assetid: e54e8ab2-fc90-4540-aed1-c6dedc2f5d88
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: DVBScramblingControlSpanningEvent, DVBScramblingControlSpanningEvent structure [Microsoft TV Technologies], _DVBScramblingControlSpanningEvent, bdamedia/DVBScramblingControlSpanningEvent, mstv.dvbscramblingcontrolspanningevent
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
req.typenames: DVBScramblingControlSpanningEvent
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	bdamedia.h
api_name:
-	DVBScramblingControlSpanningEvent
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _DVBScramblingControlSpanningEvent structure


## -description


Specifies whether a DVB program stream is scrambled.


## -struct-fields




### -field ulPID

The packet identifier (PID) associated with the stream.


### -field fScrambled

If <b>TRUE</b>, the program stream is scrambled. Otherwise, it is not scrambled.

