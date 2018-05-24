---
UID: NC:richedit.AutoCorrectProc
title: AutoCorrectProc
author: windows-driver-content
description: The AutoCorrectProc function is an application-defined callback function that is used with the EM_SETAUTOCORRECTPROC message.
old-location: controls\autocorrectproc.htm
old-project: Controls
ms.assetid: 36EF880D-F6A9-434A-820B-17E663357573
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: AutoCorrectProc, AutoCorrectProc callback, AutoCorrectProc callback function [Windows Controls], controls.autocorrectproc, richedit/AutoCorrectProc
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: richedit.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: RM_UNIQUE_PROCESS, *PRM_UNIQUE_PROCESS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Richedit.h
api_name:
-	AutoCorrectProc
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# AutoCorrectProc callback function


## -description


The <i>AutoCorrectProc</i> function is an 
    application-defined  callback function that is used with the 
    <a href="https://msdn.microsoft.com/2FA48CFC-0D7C-41EF-8207-5EDC644FF3BC">EM_SETAUTOCORRECTPROC</a> message.

<i>AutoCorrectProc</i> is a placeholder for the 
    application-defined function name. It provides application-defined automatic error correction for text entered 
    into a rich edit control.


## -parameters




### -param langid

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LANGID</a></b>

Language ID that identifies the autocorrect file to use for automatic correcting. 



### -param *pszBefore

Type: <b>const <a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">WCHAR</a>*</b>

Autocorrect candidate string. 



### -param *pszAfter

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">WCHAR</a>*</b>

Resulting autocorrect string, if the return value is not <b>ATP_NOCHANGE</b>. 



### -param cchAfter

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LONG</a></b>

Count of characters in <i>pszAfter</i>. 



### -param *pcchReplaced

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LONG</a>*</b>

Count of trailing characters in <i>pszBefore</i> to replace with <i>pszAfter</i>.


## -returns



Type: <b>int</b>

Returns one or more of the following values.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ATP_NOCHANGE</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
No change.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ATP_CHANGE</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Change but don’t replace most delimiters, and don’t replace a span of unchanged trailing characters (preserves their formatting).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ATP_NODELIMITER</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Change but don’t replace a span of unchanged trailing characters.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ATP_REPLACEALLTEXT</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
Replace trailing characters even if they are not changed (uses the same formatting for the entire replacement string). 


</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/93116467-B345-4FD9-9162-3E01CF3C6F20">EM_CALLAUTOCORRECTPROC</a>



<a href="https://msdn.microsoft.com/90821036-F27D-4AC3-9AB8-40A94486B938">EM_GETAUTOCORRECTPROC</a>



<a href="https://msdn.microsoft.com/2FA48CFC-0D7C-41EF-8207-5EDC644FF3BC">EM_SETAUTOCORRECTPROC</a>
 

 

