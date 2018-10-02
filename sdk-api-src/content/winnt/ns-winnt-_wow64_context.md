---
UID: NS:winnt._WOW64_CONTEXT
title: "_WOW64_CONTEXT"
author: windows-sdk-content
description: Represents a context frame on WOW64.
old-location: base\wow64_context.htm
tech.root: debug
ms.assetid: b27205a2-2c33-4f45-8948-9919bcd2355a
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: "*PWOW64_CONTEXT, PWOW64_CONTEXT, PWOW64_CONTEXT structure pointer, WOW64_CONTEXT, WOW64_CONTEXT structure, _WOW64_CONTEXT, base.wow64_context, winnt/PWOW64_CONTEXT, winnt/WOW64_CONTEXT"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winnt.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinNT.h
api_name:
 - WOW64_CONTEXT
product: Windows
targetos: Windows
req.typenames: WOW64_CONTEXT
req.redist: 
---

# _WOW64_CONTEXT structure


## -description


Represents a context frame on WOW64. Refer to the header file WinNT.h for the definition of this structure.


## -struct-fields


## -remarks



In the following versions of Windows, Slot 1 of Thread Local Storage (TLS) holds a pointer to a structure that contains a <b>WOW64_CONTEXT</b> structure starting at offset 4. This might change in later versions of Windows.

<table>
<tr>
<td>Windows Vista</td>
<td>Windows Server 2008</td>
</tr>
<tr>
<td>Windows 7</td>
<td>Windows Server 2008 R2</td>
</tr>
<tr>
<td>Windows 8</td>
<td>Windows Server 2012</td>
</tr>
<tr>
<td>Windows 8.1</td>
<td>Windows Server 2012 R2</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/5040CB82-D32F-4C44-8C03-30238D5B897A">Thread Environment Block (Debugging Notes)</a>



<a href="https://msdn.microsoft.com/56fba1c1-432b-40a8-b882-e4c637c03d5d">WOW64_FLOATING_SAVE_AREA</a>



<a href="https://msdn.microsoft.com/1bac28e1-3558-43c4-97e4-d8bb9514c38e">Wow64GetThreadContext</a>



<a href="https://msdn.microsoft.com/4119c945-b654-4634-a88b-e41bc762018a">Wow64SetThreadContext</a>
 

 

