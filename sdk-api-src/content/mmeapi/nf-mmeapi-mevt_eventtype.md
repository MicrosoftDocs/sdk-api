---
UID: NF:mmeapi.MEVT_EVENTTYPE
title: MEVT_EVENTTYPE macro
author: windows-sdk-content
description: The MEVT_EVENTTYPE macro retrieves the event type from the value specified in the dwEvent member of a MIDIEVENT structure.
old-location: multimedia\mevt_eventtype.htm
tech.root: Multimedia
ms.assetid: ce2ca2b4-129c-4164-ad0c-de748b4a29aa
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: MEVT_EVENTTYPE, MEVT_EVENTTYPE macro [Windows Multimedia], _win32_MEVT_EVENTTYPE, mmeapi/MEVT_EVENTTYPE, multimedia.mevt_eventtype
ms.topic: macro
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mmeapi.h
api_name:
 - MEVT_EVENTTYPE
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MEVT_EVENTTYPE macro


## -description



The <b>MEVT_EVENTTYPE</b> macro retrieves the event type from the value specified in the <b>dwEvent</b> member of a <a href="https://msdn.microsoft.com/e83bf111-2075-4cfc-a68b-e0a59a0c53e6">MIDIEVENT</a> structure.




## -parameters




### -param x

Code for the MIDI event and the event parameters or length, as specified in the dwEvent member of the MIDIEVENT structure. <i></i>


## -remarks



The <b>MEVT_EVENTTYPE</b> macro is defined as follows:


```cpp

#define MEVT_EVENTTYPE(x) ((BYTE) (((x)>>24)&0xFF)) 

```





## -see-also




<a href="https://msdn.microsoft.com/64b23c16-cf4e-4b62-bbfc-c81ea4131bfa">MIDI Macros</a>
 

 

