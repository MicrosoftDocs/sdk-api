---
UID: NF:filehc.SetDotStuffState
title: SetDotStuffState function
author: windows-sdk-content
description: Enables dot stuffing to be set in an FIO_CONTEXT structure.
old-location: winprog\_setdotstuffstate.htm
old-project: DevNotes
ms.assetid: 3acfaf74-ec36-4afb-b358-425bd5062153
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: SetDotStuffState, SetDotStuffState function [Windows API], filehc/SetDotStuffState, winprog._setdotstuffstate
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
 - SetDotStuffState
product: Windows
targetos: Windows
req.lib: Fcachdll.lib
req.dll: Fcachdll.dll
req.irql: 
req.product: Internet Explorer 5
---

# SetDotStuffState function


## -description


Enables dot stuffing to be set in an <a href="Http://go.microsoft.com/fwlink/p/?linkid=85304">FIO_CONTEXT</a> structure.


## -parameters




### -param pContext [in]

A pointer to the <a href="Http://go.microsoft.com/fwlink/p/?linkid=85304">FIO_CONTEXT</a> structure to be examined.


### -param fKnown [in]

Specifies whether the dot stuff state is known. If <b>TRUE</b>, the message requires dot stuffing and the <i>fRequiresStuffing</i> parameter becomes meaningful.


### -param fRequiresStuffing [in]

Specifies whether dot stuffing is required. If <i>fKnown</i> is  <b>TRUE</b>, <i>fRequiresStuffing</i> can be either <b>TRUE</b> or <b>FALSE</b>. If <i>fKnown</i> is <b>FALSE</b>, <i>fRequiresStuffing</i> is ignored.


## -returns



This function does not return a value.




## -see-also




<a href="Http://go.microsoft.com/fwlink/p/?linkid=85304">FIO_CONTEXT</a>
 

 

