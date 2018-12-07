---
UID: NF:msctf.ITfRange.SetText
title: ITfRange::SetText
author: windows-sdk-content
description: The ITfRange::SetText method replaces the content covered by the range of text.
old-location: tsf\itfrange_settext.htm
tech.root: TSF
ms.assetid: 797d96a1-0250-4e8d-a4bd-31152fd6eca7
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITfRange interface [Text Services Framework],SetText method, ITfRange.SetText, ITfRange::SetText, SetText, SetText method [Text Services Framework], SetText method [Text Services Framework],ITfRange interface, _tsf_itfrange_settext_ref, msctf/ITfRange::SetText, tsf.itfrange_settext
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.dll
api_name:
 - ITfRange.SetText
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfRange::SetText


## -description


The <b>ITfRange::SetText</b> method replaces the content covered by the range of text. For an empty range object, the method results in an insertion at the location of the range. If the new content is an empty string (<i>cch</i> = 0), the method deletes the existing content within the range.


## -parameters




### -param ec [in]

Identifies the edit context obtained from <a href="https://msdn.microsoft.com/1415f338-731c-44c5-b798-edf823174272">ITfDocumentMgr::CreateContext</a> or <a href="https://msdn.microsoft.com/f89b2676-9a69-492f-be8a-96e4436d594c">ITfEditSession::DoEditSession</a>.


### -param dwFlags [in]

Specifies optional behavior for correction of content. If set to the value of <a href="https://msdn.microsoft.com/fa53c1f1-50eb-45eb-b2ea-f236a376d41a">TF_ST_CORRECTION</a>, then the operation is a correction of the existing content, not a creation of new content, and original text properties are preserved.


### -param pchText [in]

Pointer to a buffer that contains the text to replace the range contents.


### -param cch [in]

Contains the number of characters in <i>pchText</i>.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TF_E_COMPOSITION_REJECTED</b></dt>
</dl>
</td>
<td width="60%">
The context owner rejected a default composition.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TF_E_NOLOCK</b></dt>
</dl>
</td>
<td width="60%">
The value of the <i>ec</i> parameter is an invalid cookie, or the caller does not have a read/write lock.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TF_E_RANGE_NOT_COVERED</b></dt>
</dl>
</td>
<td width="60%">
The range is not within the active composition of the caller.

</td>
</tr>
</table>
 




## -remarks



When a range covers multiple regions, call <b>ITfRange::SetText</b> on each region separately. Otherwise, the method can fail.

By default, text services start and end a temporary composition that covers the range, to ensure that context owners consistently recognize compositions over edited text. If the composition owner rejects a default composition, then the method returns TF_E_COMPOSITION_REJECTED. Default compositions are only created if the caller has not already started one. If the caller has an active composition, the call fails.

The <a href="https://msdn.microsoft.com/fa53c1f1-50eb-45eb-b2ea-f236a376d41a">TF_CHAR_EMBEDDED</a> object placeholder character might not be passed into this method. <a href="https://msdn.microsoft.com/95b8622d-c934-4293-abb4-9eface451be5">ITfRange::InsertEmbedded</a> should be used instead.

For inserting text, the <a href="https://msdn.microsoft.com/1373fe9b-6c51-4514-a7da-c1f872d9b1ce">ITFInsertAtSelection:InsertTextAtSelection</a> method does not require a selection range to be allocated, and avoids the requirement that the range match the selection.




## -see-also




<a href="https://msdn.microsoft.com/1373fe9b-6c51-4514-a7da-c1f872d9b1ce">ITFInsertAtSelection:InsertTextAtSelection
      </a>



<a href="https://msdn.microsoft.com/1415f338-731c-44c5-b798-edf823174272">ITfDocumentMgr::CreateContext
      </a>



<a href="https://msdn.microsoft.com/f89b2676-9a69-492f-be8a-96e4436d594c">ITfEditSession::DoEditSession
      </a>



<a href="https://msdn.microsoft.com/b8889f7d-3228-4ecc-8d24-c04234d3101e">ITfRange</a>



<a href="https://msdn.microsoft.com/b38a8de3-947f-469c-9f0d-f0482ea86884">ITfRange::GetText
      </a>



<a href="https://msdn.microsoft.com/95b8622d-c934-4293-abb4-9eface451be5">ITfRange::InsertEmbedded
      </a>



<a href="https://msdn.microsoft.com/fa53c1f1-50eb-45eb-b2ea-f236a376d41a">Miscellaneous Framework Constants</a>



<a href="https://msdn.microsoft.com/c827999a-0b74-4e5d-901e-4c2fa1d74929">Text Stores</a>
 

 

