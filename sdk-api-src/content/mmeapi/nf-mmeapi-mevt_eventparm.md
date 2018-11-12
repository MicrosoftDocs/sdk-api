---
UID: NF:mmeapi.MEVT_EVENTPARM
title: MEVT_EVENTPARM macro
author: windows-sdk-content
description: The MEVT_EVENTPARM macro retrieves the event parameters or length from the value specified in the dwEvent member of a MIDIEVENT structure.
old-location: multimedia\mevt_eventparm.htm
tech.root: Multimedia
ms.assetid: cabb6e1f-2a86-47eb-9bbb-1429cc56f485
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: MEVT_EVENTPARM, MEVT_EVENTPARM macro [Windows Multimedia], _win32_MEVT_EVENTPARM, mmeapi/MEVT_EVENTPARM, multimedia.mevt_eventparm
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - MEVT_EVENTPARM
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MEVT_EVENTPARM macro


## -description



The <b>MEVT_EVENTPARM</b> macro retrieves the event parameters or length from the value specified in the <b>dwEvent</b> member of a <a href="https://msdn.microsoft.com/e83bf111-2075-4cfc-a68b-e0a59a0c53e6">MIDIEVENT</a> structure.




## -parameters




### -param x

TBD






#### - dwEvent

Code for the MIDI event and the event parameters or length, as specified in the dwEvent member of the MIDIEVENT structure. <i></i>


## -remarks



The <b>MEVT_EVENTPARM</b> macro is defined as follows:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
#define MEVT_EVENTPARM(x) ((DWORD) ((x)&amp;0x00FFFFFFL)) 
</pre>
</td>
</tr>
</table></span></div>


