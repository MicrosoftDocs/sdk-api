---
UID: NF:fltuser.FilterInstanceClose
title: FilterInstanceClose function
author: windows-sdk-content
description: The FilterInstanceClose function closes a minifilter instance handle opened by FilterInstanceCreate.
old-location: ifsk\filterinstanceclose.htm
old-project: ifsk
ms.assetid: a0605b02-a5eb-4e7f-9659-0f0f538ea153
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: FilterInstanceClose, FilterInstanceClose function [Installable File System Drivers], FltWin32ApiRef_aed3c694-a4bb-4804-9171-4d89cabd666d.xml, fltuser/FilterInstanceClose, ifsk.filterinstanceclose
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: fltuser.h
req.include-header: Fltuser.h
req.redist: 
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
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - FltLib.dll
api_name:
 - FilterInstanceClose
product: Windows
targetos: Windows
req.lib: FltLib.lib
req.dll: FltLib.dll
req.irql: 
req.product: Internet Explorer 5
---

# FilterInstanceClose function


## -description


The <b>FilterInstanceClose</b> function closes a minifilter instance handle opened by <b>FilterInstanceCreate</b>. 


## -parameters




### -param hInstance [in]

Minifilter instance handle returned by a previous call to <a href="https://msdn.microsoft.com/eb29fefc-285a-4a77-b1f6-1d42d029b7b7">FilterInstanceCreate</a>. 


## -returns



<b>FilterInstanceClose</b> returns S_OK if successful. Otherwise, it returns an error value. 




## -remarks



After the <b>FilterInstanceClose</b> function is called, the minifilter instance handle specified by the <i>hFilterInstanceFind</i> parameter is no longer valid and cannot safely be used. 

Use <b>FilterInstanceClose</b> to close handles returned by calls to <a href="https://msdn.microsoft.com/eb29fefc-285a-4a77-b1f6-1d42d029b7b7">FilterInstanceCreate</a>. Use <a href="https://msdn.microsoft.com/f4b066ca-4154-425d-85f6-682dc7460117">FilterInstanceFindClose</a> to close handles returned by calls to <a href="https://msdn.microsoft.com/4d397383-eb65-4646-80cd-203495513285">FilterInstanceFindFirst</a>. 




## -see-also




<a href="https://msdn.microsoft.com/eb29fefc-285a-4a77-b1f6-1d42d029b7b7">FilterInstanceCreate</a>



<a href="https://msdn.microsoft.com/f4b066ca-4154-425d-85f6-682dc7460117">FilterInstanceFindClose</a>



<a href="https://msdn.microsoft.com/4d397383-eb65-4646-80cd-203495513285">FilterInstanceFindFirst</a>
 

 

