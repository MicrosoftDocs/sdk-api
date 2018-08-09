---
UID: NF:filehc.ProduceDotStuffedContext
title: ProduceDotStuffedContext function
author: windows-sdk-content
description: Retrieves the FIO_CONTEXT structure with the requested state.
old-location: winprog\_producedotstuffedcontext.htm
old-project: devnotes
ms.assetid: 6fbac935-339d-4744-9359-7b3b85bfb7c6
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ProduceDotStuffedContext, ProduceDotStuffedContext function [Windows API], filehc/ProduceDotStuffedContext, winprog._producedotstuffedcontext
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: filehc.h
req.include-header: 
req.target-type: Windows
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
req.typenames: WIN32_FIND_STREAM_DATA, *PWIN32_FIND_STREAM_DATA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Fcachdll.dll
api_name:
 - ProduceDotStuffedContext
product: Windows
targetos: Windows
req.lib: Fcachdll.lib
req.dll: Fcachdll.dll
req.irql: 
req.product: Internet Explorer 5
---

# ProduceDotStuffedContext function


## -description


Retrieves the <a href="Http://go.microsoft.com/fwlink/p/?linkid=85304">FIO_CONTEXT</a> structure with the requested state.


## -parameters




### -param pContext [in]

A pointer to an <a href="Http://go.microsoft.com/fwlink/p/?linkid=85304">FIO_CONTEXT</a> structure.


### -param lpstrName [in]

Not currently used.


### -param fWantItDotStuffed [in]

Specifies whether the <a href="Http://go.microsoft.com/fwlink/p/?linkid=85304">FIO_CONTEXT</a> structure should be dot stuffed. If <b>TRUE</b>, dots should be added. If <b>FALSE</b>, dots should be removed.


## -returns



Returns the <a href="Http://go.microsoft.com/fwlink/p/?linkid=85304">FIO_CONTEXT</a> structure.




## -remarks



This call may or may not create a new <a href="Http://go.microsoft.com/fwlink/p/?linkid=85304">FIO_CONTEXT</a> structure. If a new structure is created, it remains in the cache so that it can be used again. If a new structure is created, the user has the only reference to the resulting <a href="Http://go.microsoft.com/fwlink/p/?linkid=85304">FIO_CONTEXT</a> structure, so it disappears when <a href="Http://go.microsoft.com/fwlink/p/?linkid=85303">ReleaseContext</a> is called.




## -see-also




<a href="Http://go.microsoft.com/fwlink/p/?linkid=85304">FIO_CONTEXT</a>



<a href="Http://go.microsoft.com/fwlink/p/?linkid=85303">ReleaseContext</a>
 

 

