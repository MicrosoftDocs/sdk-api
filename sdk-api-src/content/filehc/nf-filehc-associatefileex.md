---
UID: NF:filehc.AssociateFileEx
title: AssociateFileEx function
author: windows-driver-content
description: Associates a file with an asnychronous context.
old-location: winprog\_associatefileex.htm
old-project: DevNotes
ms.assetid: b7efaa05-e6ac-4fb8-889f-ff6fa0755476
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: AssociateFileEx, AssociateFileEx function [Windows API], filehc/AssociateFileEx, winprog._associatefileex
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
-	AssociateFileEx
product: Windows
targetos: Windows
req.lib: Fcachdll.lib
req.dll: Fcachdll.dll
req.irql: 
req.product: Internet Explorer 5
---

# AssociateFileEx function


## -description


Associates a file with an asnychronous context.


## -parameters




### -param hFile [in]

A file handle that should be in the context. It is created with the FILE_FLAG_OVERLAPPED flag set for asynchronous I/O operations. 



### -param fStoreWithDots

TBD


### -param fStoredWithTerminatingDot [in]

A flag that indicates whether the terminating dot is included in an object. If this parameter is set to <b>TRUE</b>, the object is stored with a terminating dot. 

The terminating dot is used by the NNTP/SMTP protocol to identify the end of message.


#### - fStoredWithDots [in]

If set to <b>TRUE</b>, this object was stored with dot stuffing.


## -returns



Returns a pointer to the <a href="Http://go.microsoft.com/fwlink/p/?linkid=85304">FIO_CONTEXT</a> structure that was obtained. If the function fails, it returns <b>NULL</b>.




## -see-also




<a href="Http://go.microsoft.com/fwlink/p/?linkid=85304">FIO_CONTEXT</a>
 

 

