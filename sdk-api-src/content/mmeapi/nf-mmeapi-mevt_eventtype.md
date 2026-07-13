---
UID: NF:mmeapi.MEVT_EVENTTYPE
title: MEVT_EVENTTYPE macro (mmeapi.h)
description: The MEVT_EVENTTYPE macro retrieves the event type from the value specified in the dwEvent member of a MIDIEVENT structure.
helpviewer_keywords: ["MEVT_EVENTTYPE","MEVT_EVENTTYPE macro [Windows Multimedia]","_win32_MEVT_EVENTTYPE","mmeapi/MEVT_EVENTTYPE","multimedia.mevt_eventtype"]
old-location: multimedia\mevt_eventtype.htm
tech.root: Multimedia
ms.assetid: ce2ca2b4-129c-4164-ad0c-de748b4a29aa
ms.date: 07/01/2025
ms.keywords: MEVT_EVENTTYPE, MEVT_EVENTTYPE macro [Windows Multimedia], _win32_MEVT_EVENTTYPE, mmeapi/MEVT_EVENTTYPE, multimedia.mevt_eventtype
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
 - MEVT_EVENTTYPE
 - mmeapi/MEVT_EVENTTYPE
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
 - MEVT_EVENTTYPE
---

# MEVT_EVENTTYPE macro

## -syntax

```cpp
BYTE MEVT_EVENTTYPE(
    DWORD x
);
```

## -returns

Type: **[BYTE](/windows/desktop/winprog/windows-data-types)**

The event type from the value specified in the <b>dwEvent</b> member of a <a href="/previous-versions/dd798448(v=vs.85)">MIDIEVENT</a> structure.


## -description

The <b>MEVT_EVENTTYPE</b> macro retrieves the event type from the value specified in the <b>dwEvent</b> member of a <a href="/previous-versions/dd798448(v=vs.85)">MIDIEVENT</a> structure.

## -parameters

### -param x

Code for the MIDI event and the event parameters or length, as specified in the **dwEvent** member of the MIDIEVENT structure. <i></i>

## -remarks

The <b>MEVT_EVENTTYPE</b> macro is defined as follows:


```cpp

#define MEVT_EVENTTYPE(x) ((BYTE) (((x)>>24)&0xFF)) 

```

## -see-also

<a href="/windows/desktop/Multimedia/midi-macros">MIDI Macros</a>
