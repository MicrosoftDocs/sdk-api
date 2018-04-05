---
UID: NF:tom.ITextRange.GetText
title: ITextRange::GetText method
author: windows-driver-content
description: Gets the plain text in this range. The Text property is the default property of the ITextRange interface.
old-location: controls\ITextRange_GetText.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\gettext.htm
ms.author: windowsdriverdev
ms.date: 3/31/2018
ms.keywords: GetText method [Windows Controls], GetText method [Windows Controls], ITextRange interface, GetText,ITextRange.GetText, ITextRange, ITextRange interface [Windows Controls], GetText method, ITextRange::GetText, _win32_ITextRange_GetText, _win32_ITextRange_GetText_cpp, controls.ITextRange_GetText, controls._win32_ITextRange_GetText, tom/ITextRange::GetText
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
req.typenames: MANCODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Msftedit.dll
api_name:
-	ITextRange.GetText
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextRange::GetText method


## -description


Gets the plain text in this range. The Text property is the default property of the <a href="https://msdn.microsoft.com/e19678cb-f951-458c-bf96-de4b123fd63a">ITextRange</a> interface.


## -parameters




### -param pbstr

Type: <b>BSTR*</b>

The text. 


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pbstr</i> is null.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to hold the text.

</td>
</tr>
</table>
 




## -remarks



The <b>ITextRange::GetText</b> method returns the plain text in the range. The Text property is the default property for <a href="https://msdn.microsoft.com/e19678cb-f951-458c-bf96-de4b123fd63a">ITextRange</a>; this is, it is automatically invoked for a range, as  in the following Microsoft Visual Basic for Applications (VBA) example.

<code>print range</code>

Some of the examples below use this fact. The <a href="https://msdn.microsoft.com/26dd5c84-953c-4234-a0b4-53711990bce9">ITextRange::SetText</a> method substitutes <i>bstr</i> for the range text. For processing a single character, the Char property is more efficient than the Text property and does not require creating a single character range for storing a character. If the range is degenerate, the Text property lets you insert text easily. You can also delete the text in a range, as shown in the following VBA examples.
            

<code>range.delete</code>

<code>range = ""</code>

You can use the <b>Text</b> property to copy plain text from one place to another, simply by setting one range equal to another. (This is quite different from the <b>Duplicate</b> property; for more information, see <a href="https://msdn.microsoft.com/437c1571-7593-4996-8b6a-d213d7896b12">ITextRange::GetDuplicate</a>). The following Microsoft Visual Basic example statement
                sets the text in the range1 to that in range2.

<code>range1 = range2            ' Replace range1's text by range2's</code>

The ranges can be in different stories or even in different applications. However, they do imply copying the text first into a <b>BSTR</b> and then from that string to the target location. For large amounts of text, the <a href="https://msdn.microsoft.com/4e998d86-e101-4bea-8389-3760e9289151">ITextRange::Copy</a> and <a href="https://msdn.microsoft.com/62842b6f-381c-41ac-974e-9e03eae148f7">ITextRange::Paste</a> methods can be faster, since they can perform the copy directly from source to target and with any format supported by the source and target.

The text returned by the Text property is given in Unicode. The end-of-paragraph mark may be given by 0x2029 (the Unicode Paragraph Separator), or by carriage return/line feed (CR/LF) (0xd, 0xa), or by a carriage return alone, depending on the original file. Microsoft Word uses a carriage return alone, unless it reads another choice in from a file, the clipboard, or an <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a>. The placeholder for an embedded object is given by the special character, <b>WCH_EMBEDDING</b>, which has the Unicode value 0xFFFC.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff544217">Copy</a>



<a href="https://msdn.microsoft.com/437c1571-7593-4996-8b6a-d213d7896b12">GetDuplicate</a>



<a href="https://msdn.microsoft.com/e19678cb-f951-458c-bf96-de4b123fd63a">ITextRange</a>



<a href="https://msdn.microsoft.com/62842b6f-381c-41ac-974e-9e03eae148f7">Paste</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/a15f0334-1a31-4bc3-bc1e-e5cf53112007">Text Object Model</a>
 

 

