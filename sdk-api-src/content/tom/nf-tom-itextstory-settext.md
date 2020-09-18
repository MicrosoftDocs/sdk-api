---
UID: NF:tom.ITextStory.SetText
title: ITextStory::SetText (tom.h)
description: Replaces the text in a story with the specified text.
helpviewer_keywords: ["ITextStory interface [Windows Controls]","SetText method","ITextStory.SetText","ITextStory::SetText","SetText","SetText method [Windows Controls]","SetText method [Windows Controls]","ITextStory interface","controls.itextstory_settext","tom/ITextStory::SetText","tomCheckTextLimit","tomMathCFCheck","tomUnhide","tomUnicodeBiDi","tomUnlink"]
old-location: controls\itextstory_settext.htm
tech.root: Controls
ms.assetid: 9efd45ed-00f7-47e1-90e7-82a420e79bdf
ms.date: 12/05/2018
ms.keywords: ITextStory interface [Windows Controls],SetText method, ITextStory.SetText, ITextStory::SetText, SetText, SetText method [Windows Controls], SetText method [Windows Controls],ITextStory interface, controls.itextstory_settext, tom/ITextStory::SetText, tomCheckTextLimit, tomMathCFCheck, tomUnhide, tomUnicodeBiDi, tomUnlink
req.header: tom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tom.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITextStory::SetText
 - tom/ITextStory::SetText
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tom.h
api_name:
 - ITextStory.SetText
---

# ITextStory::SetText


## -description

Replaces the text in a story with the specified text.

## -parameters

### -param Flags [in]

Type: <b>long</b>

Flags controlling how the text is inserted as defined in the following table:


<a id="tomCheckTextLimit"></a>
<a id="tomchecktextlimit"></a>
<a id="TOMCHECKTEXTLIMIT"></a>


#### tomCheckTextLimit

<a id="tomMathCFCheck"></a>
<a id="tommathcfcheck"></a>
<a id="TOMMATHCFCHECK"></a>


#### tomMathCFCheck

<a id="tomUnhide"></a>
<a id="tomunhide"></a>
<a id="TOMUNHIDE"></a>


#### tomUnhide

<a id="tomUnicodeBiDi"></a>
<a id="tomunicodebidi"></a>
<a id="TOMUNICODEBIDI"></a>


#### tomUnicodeBiDi

<a id="tomUnlink"></a>
<a id="tomunlink"></a>
<a id="TOMUNLINK"></a>


#### tomUnlink

### -param bstr [in]

Type: <b>BSTR</b>

The new text for this story. If this parameter is <b>NULL</b>, the text in the story is deleted.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes. For more information about COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

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
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
Write access is denied.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextstory">ITextStory</a>



<a href="/windows/desktop/api/tom/nf-tom-itextstory-gettext">ITextStory::GetText</a>