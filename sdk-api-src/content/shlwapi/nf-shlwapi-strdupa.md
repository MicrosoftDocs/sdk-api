---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# StrDupA function


## -description


Duplicates a string.


## -parameters




### -param pszSrch

Type: <b>PCTSTR</b>

A pointer to a constant <b>null</b>-terminated character string.


## -returns



Type: <b>PTSTR</b>

Returns the address of the string that was copied, or <b>NULL</b> if the string cannot be copied.




## -remarks



<b>StrDup</b> will allocate storage the size of the original string. If storage allocation is successful, the original string is copied to the duplicate string.

This function uses <a href="https://msdn.microsoft.com/da8cd2be-ff4c-4da5-813c-8759a58228c9">LocalAlloc</a> to allocate storage space for the copy of the string. The calling application must free this memory by calling the <a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a> function on the pointer returned by the call to <b>StrDup</b>.


#### Examples

This simple console application illustrates the use of <b>StrDup</b>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#include &lt;windows.h&gt;
#include &lt;shlwapi.h&gt;
#include &lt;stdio.h&gt;

void main(void)
{
   char buffer[] = "This is the buffer text";
   char *newstring;

   // Note: Never use an unbounded %s format specifier in printf.
   printf("Original: %25s\n", buffer);

   newstring = StrDup(buffer);
   if (newstring != NULL)
   {
       printf("Copy:     %25s\n", newstring);
       LocalFree(newstring);
   }
}

OUTPUT:
- - - - - - 
Original: This is the buffer text
Copy:     This is the buffer text</pre>
</td>
</tr>
</table></span></div>


