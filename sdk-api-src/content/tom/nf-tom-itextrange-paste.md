---
UID: NF:tom.ITextRange.Paste
title: ITextRange::Paste
author: windows-sdk-content
description: Pastes text from a specified data object.
old-location: controls\ITextRange_Paste.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\paste.htm
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: ITextRange interface [Windows Controls],Paste method, ITextRange.Paste, ITextRange::Paste, Paste, Paste method [Windows Controls], Paste method [Windows Controls],ITextRange interface, _win32_ITextRange_Paste, _win32_ITextRange_Paste_cpp, controls.ITextRange_Paste, controls._win32_ITextRange_Paste, tom/ITextRange::Paste
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.lib: 
req.dll: Msftedit.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - ITextRange.Paste
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextRange::Paste


## -description


Pastes text from a specified data object. 


## -parameters




### -param pVar

Type: <b>VARIANT*</b>

The <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a> to paste. However, the contents of the clipboard are used if any of the following are true.
                

<i>pVar</i> is null 

<i>pVar</i> punkVal is null 

<i>pVar</i> is not <b>VT_UNKNOWN</b>

<i>pVar</i> punkVal does not return an <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a> when queried for one 


### -param Format

Type: <b>long</b>

The clipboard format to use in the paste operation. Zero is best format, which usually is RTF, but <b>CF_UNICODETEXT</b> and other formats are also possible. The default value is zero. For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms649013(v=VS.85).aspx">Clipboard Formats</a>.


## -returns



Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following error codes. For more information about COM error codes, see <a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling in COM</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
Destination is write-protected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Destination cannot contain the text to be pasted.

</td>
</tr>
</table>
 




## -remarks



For more information, see<a href="https://msdn.microsoft.com/en-us/library/Bb787742(v=VS.85).aspx">ITextRange::Copy</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms649013(v=VS.85).aspx">Clipboard Formats</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb787742(v=VS.85).aspx">Copy</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb774058(v=VS.85).aspx">ITextRange</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb787607(v=VS.85).aspx">Text Object Model</a>
 

 

