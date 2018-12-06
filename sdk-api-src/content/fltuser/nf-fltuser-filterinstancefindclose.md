---
UID: NF:fltuser.FilterInstanceFindClose
title: FilterInstanceFindClose function
author: windows-sdk-content
description: The FilterInstanceFindClose function closes the specified minifilter instance search handle. The FilterInstanceFindFirst and FilterInstanceFindNext functions use this search handle to locate instances of a minifilter.
old-location: ifsk\filterinstancefindclose.htm
tech.root: ifsk
ms.assetid: f4b066ca-4154-425d-85f6-682dc7460117
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: FilterInstanceFindClose, FilterInstanceFindClose function [Installable File System Drivers], FltWin32ApiRef_e9ea0ce5-7e02-40df-8e12-5b7fb8b0a189.xml, fltuser/FilterInstanceFindClose, ifsk.filterinstancefindclose
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
 - FilterInstanceFindClose
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FilterInstanceFindClose function


## -description


The <b>FilterInstanceFindClose</b> function closes the specified minifilter instance search handle. The <a href="https://msdn.microsoft.com/4d397383-eb65-4646-80cd-203495513285">FilterInstanceFindFirst</a> and <a href="https://msdn.microsoft.com/c7305378-1de8-4db0-89a2-2ac342a17620">FilterInstanceFindNext</a> functions use this search handle to locate instances of a minifilter. 


## -parameters




### -param hFilterInstanceFind [in]

Minifilter instance search handle to close. This handle must have been opened by a previous call to <a href="https://msdn.microsoft.com/4d397383-eb65-4646-80cd-203495513285">FilterInstanceFindFirst</a>. 


## -returns



<b>FilterInstanceFindClose</b> returns S_OK if successful. Otherwise, it returns an error value. 




## -remarks



After the <b>FilterInstanceFindClose</b> function is called, the minifilter instance search handle specified by the <i>hFilterInstanceFind</i> parameter cannot be used in subsequent calls to <a href="https://msdn.microsoft.com/4d397383-eb65-4646-80cd-203495513285">FilterInstanceFindFirst</a> or <b>FilterInstanceFindClose</b>. 

Use <b>FilterInstanceFindClose</b> to close handles returned by calls to <a href="https://msdn.microsoft.com/4d397383-eb65-4646-80cd-203495513285">FilterInstanceFindFirst</a>. Use <a href="https://msdn.microsoft.com/a0605b02-a5eb-4e7f-9659-0f0f538ea153">FilterInstanceClose</a> to close handles returned by calls to <a href="https://msdn.microsoft.com/eb29fefc-285a-4a77-b1f6-1d42d029b7b7">FilterInstanceCreate</a>. 




## -see-also




<a href="https://msdn.microsoft.com/a0605b02-a5eb-4e7f-9659-0f0f538ea153">FilterInstanceClose</a>



<a href="https://msdn.microsoft.com/eb29fefc-285a-4a77-b1f6-1d42d029b7b7">FilterInstanceCreate</a>



<a href="https://msdn.microsoft.com/4d397383-eb65-4646-80cd-203495513285">FilterInstanceFindFirst</a>



<a href="https://msdn.microsoft.com/c7305378-1de8-4db0-89a2-2ac342a17620">FilterInstanceFindNext</a>
 

 

