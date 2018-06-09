---
UID: NE:mfidl._MFCLOCK_RELATIONAL_FLAGS
title: "_MFCLOCK_RELATIONAL_FLAGS"
author: windows-sdk-content
description: Defines properties of a clock.
old-location: mf\mfclock_relational_flags.htm
old-project: medfound
ms.assetid: d70b432c-6ebd-405c-993f-12c4540736d7
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: MFCLOCK_RELATIONAL_FLAGS, MFCLOCK_RELATIONAL_FLAGS enumeration [Media Foundation], MFCLOCK_RELATIONAL_FLAG_JITTER_NEVER_AHEAD, _MFCLOCK_RELATIONAL_FLAGS, d70b432c-6ebd-405c-993f-12c4540736d7, mf.mfclock_relational_flags, mfidl/MFCLOCK_RELATIONAL_FLAGS, mfidl/MFCLOCK_RELATIONAL_FLAG_JITTER_NEVER_AHEAD
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MFCLOCK_RELATIONAL_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfidl.h
api_name:
 - MFCLOCK_RELATIONAL_FLAGS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _MFCLOCK_RELATIONAL_FLAGS enumeration


## -description



Defines properties of a clock.




## -enum-fields




### -field MFCLOCK_RELATIONAL_FLAG_JITTER_NEVER_AHEAD

Jitter values are always negative. In other words, the time returned by <a href="https://msdn.microsoft.com/0a897426-d994-4b27-9f13-9b0c7c9b3a9b">IMFClock::GetCorrelatedTime</a> might jitter behind the actual clock time, but will never jitter ahead of the actual time. If this flag is not present, the clock might jitter in either direction.


## -see-also




<a href="https://msdn.microsoft.com/1efc6602-9851-40e5-85aa-0335d4e899a2">MFCLOCK_PROPERTIES</a>



<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

