---
UID: NF:fltuser.FilterFindClose
title: FilterFindClose function (fltuser.h)
author: windows-sdk-content
description: The FilterFindClose function closes the specified minifilter search handle. The FilterFindFirst and FilterFindNext functions use this search handle to locate minifilters.
old-location: ifsk\filterfindclose.htm
tech.root: ifsk
ms.assetid: 053c06b0-3bfd-436c-ab98-14c55e66da53
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FilterFindClose, FilterFindClose function [Installable File System Drivers], FltWin32ApiRef_37b77edb-bee8-40ca-803f-4091417ef714.xml, fltuser/FilterFindClose, ifsk.filterfindclose
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
req.lib: FltLib.lib
req.dll: FltLib.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - FltLib.dll
api_name:
 - FilterFindClose
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# FilterFindClose function


## -description


The <b>FilterFindClose</b> function closes the specified minifilter search handle. The <a href="https://msdn.microsoft.com/e6a7c5a2-838d-47b1-ab16-aa1d27806f53">FilterFindFirst</a> and <a href="https://msdn.microsoft.com/ce56037b-d303-4efa-956f-6bbe5127efb7">FilterFindNext</a> functions use this search handle to locate minifilters. 


## -parameters




### -param hFilterFind [in]

Minifilter search handle to close. This handle must have been opened by a previous call to <a href="https://msdn.microsoft.com/e6a7c5a2-838d-47b1-ab16-aa1d27806f53">FilterFindFirst</a>. 


## -returns



<b>FilterFindClose</b> returns S_OK if successful. Otherwise, it returns an error value. 




## -remarks



After the <b>FilterFindClose</b> function is called, the minifilter search handle specified by the <i>hFilterFind</i> parameter cannot be used in subsequent calls to <a href="https://msdn.microsoft.com/ce56037b-d303-4efa-956f-6bbe5127efb7">FilterFindNext</a> or <b>FilterFindClose</b>. 

Use <b>FilterFindClose</b> to close handles returned by calls to <a href="https://msdn.microsoft.com/e6a7c5a2-838d-47b1-ab16-aa1d27806f53">FilterFindFirst</a>. Use <a href="https://msdn.microsoft.com/c5d3774e-6f57-4a6b-97a8-623268884859">FilterClose</a> to close handles returned by calls to <a href="https://msdn.microsoft.com/950e0b5b-4ee3-4eed-9039-823a6942cd38">FilterCreate</a>. 




## -see-also




<a href="https://msdn.microsoft.com/c5d3774e-6f57-4a6b-97a8-623268884859">FilterClose</a>



<a href="https://msdn.microsoft.com/950e0b5b-4ee3-4eed-9039-823a6942cd38">FilterCreate</a>



<a href="https://msdn.microsoft.com/e6a7c5a2-838d-47b1-ab16-aa1d27806f53">FilterFindFirst</a>



<a href="https://msdn.microsoft.com/ce56037b-d303-4efa-956f-6bbe5127efb7">FilterFindNext</a>
 

 

