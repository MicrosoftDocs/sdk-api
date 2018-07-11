---
UID: NF:commctrl.Header_ClearAllFilters
title: Header_ClearAllFilters macro
author: windows-sdk-content
description: Clears all of the filters for a given header control. You can use this macro or send the HDM_CLEARFILTER message explicitly.
old-location: controls\Header_ClearAllFilters.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\header\macros\header_clearallfilters.htm
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: Header_ClearAllFilters, Header_ClearAllFilters macro [Windows Controls], _win32_Header_ClearAllFilters, _win32_Header_ClearAllFilters_cpp, commctrl/Header_ClearAllFilters, controls.Header_ClearAllFilters, controls._win32_Header_ClearAllFilters
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: STGOPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - Header_ClearAllFilters
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# Header_ClearAllFilters macro


## -description


Clears all of the filters for a given header control. You can use this macro or send the <a href="https://msdn.microsoft.com/74c0265e-68d1-4414-8fd9-20f5f041d4b4">HDM_CLEARFILTER</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the header control. 


## -remarks



When all the filters are cleared, the <a href="https://msdn.microsoft.com/0a46af14-569a-4119-881f-549a130f9b0d">HDN_FILTERCHANGE</a> notification will be sent only once. 




## -see-also




<a href="https://msdn.microsoft.com/d52e4636-9d08-42fc-8e64-e07245183c91">Header_ClearFilter</a>
 

 

