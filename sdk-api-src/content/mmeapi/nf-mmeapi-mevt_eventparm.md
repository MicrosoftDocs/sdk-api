---
UID: NF:mmeapi.MEVT_EVENTPARM
title: MEVT_EVENTPARM macro (mmeapi.h)
description: The MEVT_EVENTPARM macro retrieves the event parameters or length from the value specified in the dwEvent member of a MIDIEVENT structure.
helpviewer_keywords: ["MEVT_EVENTPARM","MEVT_EVENTPARM macro [Windows Multimedia]","_win32_MEVT_EVENTPARM","mmeapi/MEVT_EVENTPARM","multimedia.mevt_eventparm"]
old-location: multimedia\mevt_eventparm.htm
tech.root: Multimedia
ms.assetid: cabb6e1f-2a86-47eb-9bbb-1429cc56f485
ms.date: 07/01/2025
ms.keywords: MEVT_EVENTPARM, MEVT_EVENTPARM macro [Windows Multimedia], _win32_MEVT_EVENTPARM, mmeapi/MEVT_EVENTPARM, multimedia.mevt_eventparm
req.header: mmeapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - MEVT_EVENTPARM
 - mmeapi/MEVT_EVENTPARM
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mmeapi.h
api_name:
 - MEVT_EVENTPARM
---

# MEVT_EVENTPARM macro

## -syntax

```cpp
DWORD MEVT_EVENTPARM(
    DWORD x
);
```

## -returns

Type: **[DWORD](/windows/desktop/winprog/windows-data-types)**

The event parameters or length from the value specified in the <b>dwEvent</b> member of a <a href="/previous-versions/dd798448(v=vs.85)">MIDIEVENT</a> structure.


## -description

The <b>MEVT_EVENTPARM</b> macro retrieves the event parameters or length from the value specified in the <b>dwEvent</b> member of a <a href="/previous-versions/dd798448(v=vs.85)">MIDIEVENT</a> structure.

## -parameters

### -param x

Code for the MIDI event and the event parameters or length, as specified in the dwEvent member of the MIDIEVENT structure. <i></i>

## -remarks

The <b>MEVT_EVENTPARM</b> macro is defined as follows:


```cpp

#define MEVT_EVENTPARM(x) ((DWORD) ((x)&0x00FFFFFFL)) 

```
