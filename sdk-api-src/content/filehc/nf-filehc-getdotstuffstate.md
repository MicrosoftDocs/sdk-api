---
UID: NF:filehc.GetDotStuffState
title: GetDotStuffState function
author: windows-driver-content
description: Determines whether dots are added to the file when any dot stuffing mechanisms are turned on.
old-location: winprog\_getdotstuffstate.htm
old-project: DevNotes
ms.assetid: 069d9cc9-0478-457a-826b-2e4d1e1b0b05
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: GetDotStuffState, GetDotStuffState function [Windows API], filehc/GetDotStuffState, winprog._getdotstuffstate
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: CREATEFILE2_EXTENDED_PARAMETERS, *PCREATEFILE2_EXTENDED_PARAMETERS, *LPCREATEFILE2_EXTENDED_PARAMETERS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Fcachdll.dll
api_name:
-	GetDotStuffState
product: Windows
targetos: Windows
req.lib: Fcachdll.lib
req.dll: Fcachdll.dll
req.irql: 
req.product: Internet Explorer 5
---

# GetDotStuffState function


## -description


Determines whether dots are added to the file when any dot stuffing mechanisms are turned on.


## -parameters




### -param pContext [in]

A pointer to the <a href="Http://go.microsoft.com/fwlink/p/?linkid=85304">FIO_CONTEXT</a> structure.


### -param fReads [in]

Indicates the dot stuff states that resulted from reads or from writes. If <b>TRUE</b>, the states of Reads are provided. If <b>FALSE</b>, the states of Writes are provided.


### -param pfStuffed [out]

Indicates whether any dots were processed, scanned, or modified. If no dots were processed, scanned, or modified, this value is <b>FALSE</b>; otherwise, it is <b>TRUE</b>. 

<div class="alert"><b>Note</b>  This parameter cannot be set to <b>NULL</b>.</div>
<div> </div>

### -param pfStoredWithDots [out]

Indicates whether the file was stored with stuffed dots.


## -returns



Returns <b>TRUE</b> if the dot stuff state is known; otherwise, it returns <b>FALSE</b>.




## -remarks



The information about dot stuffing is provided by DOT_STUFF_MANAGER objects.




## -see-also




<a href="Http://go.microsoft.com/fwlink/p/?linkid=85304">FIO_CONTEXT</a>
 

 

