---
UID: NF:imm.ImmEnumInputContext
title: ImmEnumInputContext function
author: windows-sdk-content
description: Retrieves the input context for the specified thread.
old-location: intl\immenuminputcontext.htm
old-project: Intl
ms.assetid: b066af9a-5bcc-468b-bc1b-79b549a9e55c
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: 0, 1, ImmEnumInputContext, ImmEnumInputContext function [Internationalization for Windows Applications], Thread ID, _win32_ImmEnumInputContext, imm/ImmEnumInputContext, intl.immenuminputcontext
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: imm.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only],East Asian language support installed.
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: IMECOMPOSITIONSTRINGINFO, *LPIMECOMPOSITIONSTRINGINFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Imm32.dll
api_name:
-	ImmEnumInputContext
product: Windows
targetos: Windows
req.lib: Imm32.lib
req.dll: Imm32.dll
req.irql: 
req.product: GDI+ 1.1
---

# ImmEnumInputContext function


## -description


Retrieves the input context for the specified thread.


## -parameters




### -param idThread [in]

Identifier for the thread. This parameter can have one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="0"></a><dl>
<dt><b>0</b></dt>
</dl>
</td>
<td width="60%">
Current thread.

</td>
</tr>
<tr>
<td width="40%"><a id="1"></a><dl>
<dt><b>1</b></dt>
</dl>
</td>
<td width="60%">
Current process.

</td>
</tr>
<tr>
<td width="40%"><a id="Thread_ID"></a><a id="thread_id"></a><a id="THREAD_ID"></a><dl>
<dt><b>Thread ID</b></dt>
</dl>
</td>
<td width="60%">
Identifier of the thread for which to enumerate the context. This thread identifier can belong to another process.

</td>
</tr>
</table>
 


### -param lpfn [in]

Pointer to the enumeration callback function. For more information, see <a href="https://msdn.microsoft.com/c66dcc0f-733a-44a2-942f-f518b752d014">EnumInputContext</a>.


### -param lParam [in]

Application-supplied data. The function passes this data to the callback function.


## -returns



Returns <b>TRUE</b> if successful or <b>FALSE</b> otherwise.




## -remarks



This function calls the application callback function for each enumerated input context, and passes the specified <i>lParam</i> value.




## -see-also




<a href="https://msdn.microsoft.com/c66dcc0f-733a-44a2-942f-f518b752d014">EnumInputContext</a>



<a href="https://msdn.microsoft.com/3e23e004-514a-4021-bd20-5ac55547258f">Input Method Manager</a>



<a href="https://msdn.microsoft.com/833c07eb-0ecf-41e2-9e01-8d83e51ffcef">Input Method Manager Functions</a>
 

 

