---
UID: NF:fltuser.FilterFindClose
title: FilterFindClose function
author: windows-driver-content
description: The FilterFindClose function closes the specified minifilter search handle. The FilterFindFirst and FilterFindNext functions use this search handle to locate minifilters.
old-location: ifsk\filterfindclose.htm
old-project: ifsk
ms.assetid: 053c06b0-3bfd-436c-ab98-14c55e66da53
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: FilterFindClose, FilterFindClose function [Installable File System Drivers], FltWin32ApiRef_37b77edb-bee8-40ca-803f-4091417ef714.xml, fltuser/FilterFindClose, ifsk.filterfindclose
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: fltuser.h
req.include-header: Fltuser.h
req.target-type: Universal
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: FILTERED_DATA_SOURCES
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	FltLib.dll
api_name:
-	FilterFindClose
product: Windows
targetos: Windows
req.lib: FltLib.lib
req.dll: FltLib.dll
req.irql: 
req.product: Internet Explorer 5
---

# FilterFindClose function


## -description


The <b>FilterFindClose</b> function closes the specified minifilter search handle. The <a href="https://msdn.microsoft.com/library/windows/hardware/ff540485">FilterFindFirst</a> and <a href="https://msdn.microsoft.com/library/windows/hardware/ff540488">FilterFindNext</a> functions use this search handle to locate minifilters. 


## -parameters




### -param hFilterFind [in]

Minifilter search handle to close. This handle must have been opened by a previous call to <a href="https://msdn.microsoft.com/library/windows/hardware/ff540485">FilterFindFirst</a>. 


## -returns



<b>FilterFindClose</b> returns S_OK if successful. Otherwise, it returns an error value. 




## -remarks



After the <b>FilterFindClose</b> function is called, the minifilter search handle specified by the <i>hFilterFind</i> parameter cannot be used in subsequent calls to <a href="https://msdn.microsoft.com/library/windows/hardware/ff540488">FilterFindNext</a> or <b>FilterFindClose</b>. 

Use <b>FilterFindClose</b> to close handles returned by calls to <a href="https://msdn.microsoft.com/library/windows/hardware/ff540485">FilterFindFirst</a>. Use <a href="https://msdn.microsoft.com/library/windows/hardware/ff540453">FilterClose</a> to close handles returned by calls to <a href="https://msdn.microsoft.com/library/windows/hardware/ff540467">FilterCreate</a>. 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff540453">FilterClose</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff540467">FilterCreate</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff540485">FilterFindFirst</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff540488">FilterFindNext</a>
 

 

