---
UID: NF:tom.ITextRange.GetFormattedText
title: ITextRange::GetFormattedText (tom.h)
author: windows-sdk-content
description: Gets an ITextRange object with the specified range's formatted text.
old-location: controls\ITextRange_GetFormattedText.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\getformattedtext.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetFormattedText, GetFormattedText method [Windows Controls], GetFormattedText method [Windows Controls],ITextRange interface, ITextRange interface [Windows Controls],GetFormattedText method, ITextRange.GetFormattedText, ITextRange::GetFormattedText, _win32_ITextRange_GetFormattedText, _win32_ITextRange_GetFormattedText_cpp, controls.ITextRange_GetFormattedText, controls._win32_ITextRange_GetFormattedText, tom/ITextRange::GetFormattedText
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
 - ITextRange.GetFormattedText
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITextRange::GetFormattedText


## -description


Gets an <a href="https://docs.microsoft.com/windows/desktop/api/tom/nn-tom-itextrange">ITextRange</a> object with the specified range's formatted text.


## -parameters




### -param ppRange

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/tom/nn-tom-itextrange">ITextRange</a>**</b>

The <a href="https://docs.microsoft.com/windows/desktop/api/tom/nn-tom-itextrange">ITextRange</a> object with the formatted text. 


## -returns



Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following error codes. For more information about COM error codes, see <a href="https://docs.microsoft.com/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

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
<i>ppRange</i> is null.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Out of memory.

</td>
</tr>
</table>
 




## -remarks



This method, which amounts to an alias for the <a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrange-getduplicate">ITextRange::GetDuplicate</a> method, is included to be Microsoft Visual Basic for Applications (VBA)-friendly. The method returns the formatted text in a range. If the <a href="https://docs.microsoft.com/windows/desktop/api/tom/nn-tom-itextrange">ITextRange</a> does not belong to the same Text Object Model (TOM) engine, call <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)">IUnknown::QueryInterface</a> for an <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> interface. 

Among the formats typically supported by <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> are <b>CF_TEXT</b> and <b>CF_RTF</b>. In addition, private formats can be used to reference a text solution's own internal rich-text formats. The following Microsoft Visual Basic example uses the <b>FormattedText</b> property to replace the text in a range2, by the formatted text in range1. 
            

<code>range2.FormattedText = range1.FormattedText</code>




## -see-also




<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/api/tom/nn-tom-itextrange">ITextRange</a>



<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrange-setformattedtext">SetFormattedText</a>



<a href="https://docs.microsoft.com/windows/desktop/Controls/text-object-model">Text Object Model</a>
 

 

