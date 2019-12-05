---
UID: NF:tom.ITextDocument.GetName
title: ITextDocument::GetName (tom.h)
description: Gets the file name of this document. This is the ITextDocument default property.
old-location: controls\ITextDocument_GetName.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\itextdocument\itextdocumentgetname.htm
ms.date: 12/05/2018
ms.keywords: GetName, GetName method [Windows Controls], GetName method [Windows Controls],ITextDocument interface, ITextDocument interface [Windows Controls],GetName method, ITextDocument.GetName, ITextDocument::GetName, _win32_ITextDocument_GetName, _win32_ITextDocument_GetName_cpp, controls.ITextDocument_GetName, controls._win32_ITextDocument_GetName, tom/ITextDocument::GetName
ms.topic: method
f1_keywords:
- tom/ITextDocument.GetName
dev_langs:
- c++
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
- ITextDocument.GetName
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITextDocument::GetName


## -description


Gets the file name of this document. This is the <a href="https://docs.microsoft.com/windows/desktop/api/tom/nn-tom-itextdocument">ITextDocument</a> default property.


## -parameters




### -param pName

Type: <b>BSTR*</b>

The file name. 


## -returns



Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes. For more information about COM error codes, see <a href="https://docs.microsoft.com/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
No file name associated with this object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory for output string.

</td>
</tr>
</table>
 




## -see-also




<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/api/tom/nn-tom-itextdocument">ITextDocument</a>



<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/Controls/text-object-model">Text Object Model</a>
 

 

