---
UID: NF:fltuser.FilterInstanceFindClose
title: FilterInstanceFindClose function
author: windows-sdk-content
description: The FilterInstanceFindClose function closes the specified minifilter instance search handle. The FilterInstanceFindFirst and FilterInstanceFindNext functions use this search handle to locate instances of a minifilter.
old-location: ifsk\filterinstancefindclose.htm
old-project: ifsk
ms.assetid: f4b066ca-4154-425d-85f6-682dc7460117
ms.author: windowssdkdev
ms.date: 04/16/2018
ms.keywords: FilterInstanceFindClose, FilterInstanceFindClose function [Installable File System Drivers], FltWin32ApiRef_e9ea0ce5-7e02-40df-8e12-5b7fb8b0a189.xml, fltuser/FilterInstanceFindClose, ifsk.filterinstancefindclose
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: FILTERED_DATA_SOURCES
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	FltLib.dll
api_name:
-	FilterInstanceFindClose
product: Windows
targetos: Windows
req.lib: FltLib.lib
req.dll: FltLib.dll
req.irql: 
req.product: Internet Explorer 5
---

# FilterInstanceFindClose function


## -description


The <b>FilterInstanceFindClose</b> function closes the specified minifilter instance search handle. The <a href="https://msdn.microsoft.com/library/windows/hardware/ff540541">FilterInstanceFindFirst</a> and <a href="https://msdn.microsoft.com/library/windows/hardware/ff541493">FilterInstanceFindNext</a> functions use this search handle to locate instances of a minifilter. 


## -parameters




### -param hFilterInstanceFind [in]

Minifilter instance search handle to close. This handle must have been opened by a previous call to <a href="https://msdn.microsoft.com/library/windows/hardware/ff540541">FilterInstanceFindFirst</a>. 


## -returns



<b>FilterInstanceFindClose</b> returns S_OK if successful. Otherwise, it returns an error value. 




## -remarks



After the <b>FilterInstanceFindClose</b> function is called, the minifilter instance search handle specified by the <i>hFilterInstanceFind</i> parameter cannot be used in subsequent calls to <a href="https://msdn.microsoft.com/library/windows/hardware/ff540541">FilterInstanceFindFirst</a> or <b>FilterInstanceFindClose</b>. 

Use <b>FilterInstanceFindClose</b> to close handles returned by calls to <a href="https://msdn.microsoft.com/library/windows/hardware/ff540541">FilterInstanceFindFirst</a>. Use <a href="https://msdn.microsoft.com/library/windows/hardware/ff540524">FilterInstanceClose</a> to close handles returned by calls to <a href="https://msdn.microsoft.com/library/windows/hardware/ff540528">FilterInstanceCreate</a>. 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff540524">FilterInstanceClose</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff540528">FilterInstanceCreate</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff540541">FilterInstanceFindFirst</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff541493">FilterInstanceFindNext</a>
 

 

