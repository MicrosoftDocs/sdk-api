---
UID: NF:commctrl.Header_ClearFilter
title: Header_ClearFilter macro
author: windows-sdk-content
description: Clears the filter for a given header control. You can use this macro or send the HDM_CLEARFILTER message explicitly.
old-location: controls\Header_ClearFilter.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\header\macros\header_clearfilter.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: Header_ClearFilter, Header_ClearFilter macro [Windows Controls], _win32_Header_ClearFilter, _win32_Header_ClearFilter_cpp, commctrl/Header_ClearFilter, controls.Header_ClearFilter, controls._win32_Header_ClearFilter
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - Commctrl.h
api_name:
 - Header_ClearFilter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- HeaderDef
: 
- commctrl.h
: 
- Header_ClearFilter
: 
---

# Header_ClearFilter macro


## -description


Clears the filter for a given header control. You can use this macro or send the <a href="https://msdn.microsoft.com/74c0265e-68d1-4414-8fd9-20f5f041d4b4">HDM_CLEARFILTER</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the header control. 


### -param i

Type: <b>int</b>

A value specifying the column of the filter to be cleared. Specifying -1 will clear all of the filters. 


## -remarks



If the column value is specified as -1, all the filters will be cleared and the <a href="https://msdn.microsoft.com/0a46af14-569a-4119-881f-549a130f9b0d">HDN_FILTERCHANGE</a> notification will be sent only once. 




## -see-also




<a href="https://msdn.microsoft.com/2b789b52-d083-46ee-b032-fe24771b3193">Header_ClearAllFilters</a>
 

 

