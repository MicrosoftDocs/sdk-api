---
UID: NF:textstor.ITextStoreAnchorSink.OnTextChange
title: ITextStoreAnchorSink::OnTextChange (textstor.h)
author: windows-sdk-content
description: ITextStoreAnchorSink::OnTextChange method
old-location: tsf\itextstoreanchorsink_ontextchange.htm
tech.root: TSF
ms.assetid: 4bdf12bc-c15e-4bdb-8bc0-53172e9c943e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 0, ITextStoreAnchorSink interface [Text Services Framework],OnTextChange method, ITextStoreAnchorSink.OnTextChange, ITextStoreAnchorSink::OnTextChange, OnTextChange, OnTextChange method [Text Services Framework], OnTextChange method [Text Services Framework],ITextStoreAnchorSink interface, TS_TC_CORRECTION, _tsf_itextstoreanchorsink_ontextchange_ref, textstor/ITextStoreAnchorSink::OnTextChange, tsf.itextstoreanchorsink_ontextchange
ms.topic: method
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Textstor.idl
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
 - msctf.dll
api_name:
 - ITextStoreAnchorSink.OnTextChange
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITextStoreAnchorSink::OnTextChange


## -description




## -parameters




### -param dwFlags [in]

Contains a set of flags that specify additional information about the text change. This can be one or more of the following values.

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
The text has changed.

</td>
</tr>
<tr>
<td width="40%"><a id="TS_TC_CORRECTION"></a><a id="ts_tc_correction"></a><dl>
<dt><b>TS_TC_CORRECTION</b></dt>
</dl>
</td>
<td width="60%">
The text is a transform (correction) of existing content, and any special text markup information (metadata) is retained, such as .wav file data or a language identifier. This flag is used for applications that need to preserve data associated with the original text.

</td>
</tr>
</table>
 


### -param paStart [in]

Pointer to an anchor located at the start of the changed text.


### -param paEnd [in]

Pointer to an anchor located at the end of the changed text.


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
The method was unable to create cloned anchors to contain the change.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>paStart</i> or <i>paEnd</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation failure occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TS_E_NOLOCK</b></dt>
</dl>
</td>
<td width="60%">
The TSF manager holds a lock on the document. This typically indicates that the method was called from within another <a href="https://msdn.microsoft.com/62730a6d-4dc8-4207-9818-ab95e6537854">ITextStoreAnchor</a> method, such as <a href="https://msdn.microsoft.com/03beac03-cd09-4e03-b700-d96741e4932b">ITextStoreAnchor::SetText</a>.

</td>
</tr>
</table>
 




## -remarks



This method is called only when the application modifies its own text, not when a client modifies text with one of the <b>ITextStoreAnchor</b> methods, such as <b>ITextStoreAnchor::SetText</b> or <a href="https://msdn.microsoft.com/f5cb512a-d9f5-451f-b6cb-2020ba32e855">ITextStoreAnchor::InsertTextAtSelection</a>.

When calling this method, the application must be able to grant a <a href="https://msdn.microsoft.com/3c623c44-b0d3-4b03-8de9-25f1062b5726">document lock</a>.




## -see-also




<a href="https://msdn.microsoft.com/3c623c44-b0d3-4b03-8de9-25f1062b5726">Document Locks</a>



<a href="https://msdn.microsoft.com/62730a6d-4dc8-4207-9818-ab95e6537854">ITextStoreAnchor
      </a>



<a href="https://msdn.microsoft.com/f5cb512a-d9f5-451f-b6cb-2020ba32e855">ITextStoreAnchor::InsertTextAtSelection
      </a>



<a href="https://msdn.microsoft.com/03beac03-cd09-4e03-b700-d96741e4932b">ITextStoreAnchor::SetText
      </a>



<a href="https://msdn.microsoft.com/fb96b4fb-864f-4f32-bf7c-cf7f199e552a">ITextStoreAnchorSink</a>



<a href="https://msdn.microsoft.com/6e05ed74-fff3-4bc4-a21e-9af9492af23b">Miscellaneous Text Store Constants
      </a>
 

 

