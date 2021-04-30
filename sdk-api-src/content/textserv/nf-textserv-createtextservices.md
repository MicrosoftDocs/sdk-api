---
UID: NF:textserv.CreateTextServices
title: CreateTextServices function (textserv.h)
description: The CreateTextServices function creates an instance of a text services object. The text services object supports a variety of interfaces, including ITextServices and the Text Object Model (TOM).
helpviewer_keywords: ["CreateTextServices","CreateTextServices function [Windows Controls]","_win32_CreateTextServices","_win32_CreateTextServices_cpp","controls.CreateTextServices","controls._win32_CreateTextServices","textserv/CreateTextServices"]
old-location: controls\CreateTextServices.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolfunctions\createtextservices.htm
ms.date: 12/05/2018
ms.keywords: CreateTextServices, CreateTextServices function [Windows Controls], _win32_CreateTextServices, _win32_CreateTextServices_cpp, controls.CreateTextServices, controls._win32_CreateTextServices, textserv/CreateTextServices
req.header: textserv.h
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
req.lib: Riched20.lib
req.dll: Msftedit.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CreateTextServices
 - textserv/CreateTextServices
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msftedit.dll
api_name:
 - CreateTextServices
---

# CreateTextServices function


## -description

The <b>CreateTextServices</b> function creates an instance of a text services object. The text services object supports a variety of interfaces, including <a href="/windows/desktop/api/textserv/nl-textserv-itextservices">ITextServices</a> and the 
			Text Object Model (TOM).

## -parameters

### -param punkOuter [in]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

Pointer to the controlling <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface on the outer object if the text services object is being created as part of an aggregate object. This parameter can be <b>NULL</b> if the object is not part of an aggregate.

### -param pITextHost [in]

Type: <b><a href="/windows/desktop/api/textserv/nl-textserv-itexthost">ITextHost</a>*</b>

Pointer to your implementation of the <a href="/windows/desktop/api/textserv/nl-textserv-itexthost">ITextHost</a> interface. This pointer must not be <b>NULL</b>.

### -param ppUnk [out]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>**</b>

Pointer to a variable that receives a pointer to the private <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> of the text services object. You can call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> on this pointer to retrieve <a href="/windows/desktop/api/textserv/nl-textserv-itextservices">ITextServices</a> or <a href="/windows/desktop/api/tom/nn-tom-itextdocument">ITextDocument</a> interface pointers.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the text services object was created successfully, the return value is S_OK. 

If the function fails, one of the following COM error codes are returned. For more information on COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>. 

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
An invalid argument was passed in.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Memory for text services object could not be allocated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The text services object could not be initialized.

</td>
</tr>
</table>

## -remarks

A text services object can be created as part of a standard COM-aggregated object. If it is, then callers should follow standard OLE32 rules for dealing with aggregated objects and caching interface pointers obtained through <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> from the private <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nn-tom-itextdocument">ITextDocument</a>



<a href="/windows/desktop/api/textserv/nl-textserv-itexthost">ITextHost</a>



<a href="/windows/desktop/api/textserv/nl-textserv-itextservices">ITextServices</a>



<b>Reference</b>



<a href="/windows/desktop/Controls/windowless-rich-edit-controls">Windowless Rich Edit Controls</a>