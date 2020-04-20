---
UID: NF:commctrl.Header_ClearFilter
title: Header_ClearFilter macro (commctrl.h)
description: Clears the filter for a given header control. You can use this macro or send the HDM_CLEARFILTER message explicitly.helpviewer_keywords: ["Header_ClearFilter","Header_ClearFilter macro [Windows Controls]","_win32_Header_ClearFilter","_win32_Header_ClearFilter_cpp","commctrl/Header_ClearFilter","controls.Header_ClearFilter","controls._win32_Header_ClearFilter"]
old-location: controls\Header_ClearFilter.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\header\macros\header_clearfilter.htm
ms.date: 12/05/2018
ms.keywords: Header_ClearFilter, Header_ClearFilter macro [Windows Controls], _win32_Header_ClearFilter, _win32_Header_ClearFilter_cpp, commctrl/Header_ClearFilter, controls.Header_ClearFilter, controls._win32_Header_ClearFilter
f1_keywords:
- commctrl/Header_ClearFilter
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# Header_ClearFilter macro


## -description


Clears the filter for a given header control. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/hdm-clearfilter">HDM_CLEARFILTER</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the header control. 


### -param i

Type: <b>int</b>

A value specifying the column of the filter to be cleared. Specifying -1 will clear all of the filters. 


## -remarks



If the column value is specified as -1, all the filters will be cleared and the <a href="https://docs.microsoft.com/windows/desktop/Controls/hdn-filterchange">HDN_FILTERCHANGE</a> notification will be sent only once. 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/commctrl/nf-commctrl-header_clearallfilters">Header_ClearAllFilters</a>
 

 

