---
UID: NF:oleauto.SysStringByteLen
title: SysStringByteLen function
author: windows-driver-content
description: Returns the length (in bytes) of a BSTR.
old-location: automat\sysstringbytelen.htm
old-project: automat
ms.assetid: 2a150503-f474-41b8-90dd-fbbc955bea99
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: SysStringByteLen, SysStringByteLen function [Automation], _oa96_SysStringByteLen, automat.sysstringbytelen, oleauto/SysStringByteLen
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: oleauto.h
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
req.typenames: REGKIND
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	OleAut32.dll
api_name:
-	SysStringByteLen
product: Windows
targetos: Windows
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# SysStringByteLen function


## -description


Returns the length (in bytes) of a BSTR.


## -parameters




### -param bstr [in, optional]

A previously allocated string.


## -returns



The number of bytes in <i>bstr</i>, not including the terminating null character. If <i>bstr</i> is null the return value is zero.




## -remarks



The returned value may be different from <b>strlen</b>(bstr) if the BSTR contains embedded null characters. This function always returns the number of bytes specified in the len parameter of the <a href="https://msdn.microsoft.com/e7f49441-eff1-4c00-b61f-8522c4e250ef">SysAllocStringByteLen</a> function used to allocate the BSTR.




## -see-also




<a href="https://msdn.microsoft.com/323cefbf-836c-4c9d-bcbe-f2663a57d2b5">String Manipulation Functions</a>
 

 

