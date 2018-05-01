---
UID: NF:oleauto.SysAllocStringLen
title: SysAllocStringLen function
author: windows-driver-content
description: Allocates a new string, copies the specified number of characters from the passed string, and appends a null-terminating character.
old-location: automat\sysallocstringlen.htm
old-project: automat
ms.assetid: f98bff39-bc5f-4a81-85d7-d5228e20fbc8
ms.author: windowsdriverdev
ms.date: 4/20/2018
ms.keywords: SysAllocStringLen, SysAllocStringLen function [Automation], _oa96_SysAllocStringLen, automat.sysallocstringlen, oleauto/SysAllocStringLen
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
-	SysAllocStringLen
product: Windows
targetos: Windows
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# SysAllocStringLen function


## -description


Allocates a new string, copies the specified number of characters from the passed string, and appends a null-terminating character.


## -parameters




### -param strIn [in]

The input string.


### -param ui [in]

The number of characters to copy. A null character is placed afterwards, allocating a total of <i>ui</i> plus one characters.


## -returns



A copy of the string, or <b>NULL</b> if there is insufficient memory to complete the operation.




## -remarks



The string can contain embedded null characters and does not need to end with a <b>NULL</b>. Free the returned string later with <a href="https://msdn.microsoft.com/8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a>. If <i>strIn</i> is not <b>NULL</b>, then the memory allocated to <i>strIn</i> must be at least <i>ui</i> characters long.

<div class="alert"><b>Note</b>  This function does not convert a <b>char *</b> string into a Unicode <b>BSTR</b>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/323cefbf-836c-4c9d-bcbe-f2663a57d2b5">String Manipulation Functions</a>
 

 

