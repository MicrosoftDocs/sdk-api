---
UID: NF:msctf.ITfRange.InsertEmbedded
title: ITfRange::InsertEmbedded
author: windows-sdk-content
description: The ITfRange::InsertEmbedded method inserts an object at the location of the start anchor of the range of text.
old-location: tsf\itfrange_insertembedded.htm
old-project: TSF
ms.assetid: 95b8622d-c934-4293-abb4-9eface451be5
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITfRange interface [Text Services Framework],InsertEmbedded method, ITfRange.InsertEmbedded, ITfRange::InsertEmbedded, InsertEmbedded, InsertEmbedded method [Text Services Framework], InsertEmbedded method [Text Services Framework],ITfRange interface, _tsf_itfrange_insertembedded_ref, msctf/ITfRange::InsertEmbedded, tsf.itfrange_insertembedded
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msctf.h
req.include-header: 
req.redist: TSF 1.0 on Windows 2000 Professional
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
tech.root: 
req.typenames: TF_DA_ATTR_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.dll
api_name:
 - ITfRange.InsertEmbedded
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfRange::InsertEmbedded


## -description


The <b>ITfRange::InsertEmbedded</b> method inserts an object at the location of the start anchor of the range of text.


## -parameters




### -param ec [in]

Edit cookie obtained from <a href="https://msdn.microsoft.com/1415f338-731c-44c5-b798-edf823174272">ITfDocumentMgr::CreateContext</a> or <a href="https://msdn.microsoft.com/f89b2676-9a69-492f-be8a-96e4436d594c">ITfEditSession::DoEditSession</a>.


### -param dwFlags [in]

Bit fields that specify how insertion should occur. If <a href="https://msdn.microsoft.com/fa53c1f1-50eb-45eb-b2ea-f236a376d41a">TF_IE_CORRECTION</a> is set, the operation is a correction, so that other text services can preserve data associated with the original text.


### -param pDataObject [in]

Pointer to the data transfer object to be inserted.


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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The implementing application does not expose embedded objects in its stream.

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
<dt><b>TF_E_FORMAT</b></dt>
</dl>
</td>
<td width="60%">
The context owner cannot handle the specified object type.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TF_E_NOLOCK</b></dt>
</dl>
</td>
<td width="60%">
The value of the <i>ec</i> parameter is an invalid cookie, or the caller does not have a read-only lock.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TF_E_RANGE_NOT_COVERED</b></dt>
</dl>
</td>
<td width="60%">
The caller already has an active composition, but the range is positioned over text not covered by the composition.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TF_E_READONLY</b></dt>
</dl>
</td>
<td width="60%">
The document or the location of the range cannot be modified.

</td>
</tr>
</table>
 




## -remarks



Use this method to insert objects into the text stream, because the <a href="https://msdn.microsoft.com/fa53c1f1-50eb-45eb-b2ea-f236a376d41a">TF_CHAR_EMBEDDED</a> object placeholder character cannot be passed into <a href="https://msdn.microsoft.com/797d96a1-0250-4e8d-a4bd-31152fd6eca7">ITfRange::SetText</a>. This method is modeled after the OLE clipboard API, with applications using <i>pDataObject</i> as they would an <a href="_ole_idataobject">IDataObject</a> returned from OleGetClipboard.

When a range covers multiple regions, the method should be called on each region separately. Otherwise, the method might fail.

By default, text services start and end a temporary composition that covers the range, to ensure that context owners consistently recognize compositions over edited text. If the composition owner rejects a default composition, then the method returns TF_E_COMPOSITION_REJECTED. Default compositions are only created if the caller has not already started one. If the caller has an active composition, the call fails.

To determine in advance whether a context owner supports insertion of a particular object, use <a href="https://msdn.microsoft.com/52f9465f-725e-493b-89ee-1b3db3cef696">ITfQueryEmbedded::QueryInsertEmbedded</a>.




## -see-also




<a href="_ole_idataobject">IDataObject</a>



<a href="https://msdn.microsoft.com/1415f338-731c-44c5-b798-edf823174272">ITfDocumentMgr::CreateContext
      </a>



<a href="https://msdn.microsoft.com/f89b2676-9a69-492f-be8a-96e4436d594c">ITfEditSession::DoEditSession
      </a>



<a href="https://msdn.microsoft.com/b8889f7d-3228-4ecc-8d24-c04234d3101e">ITfRange</a>



<a href="https://msdn.microsoft.com/ff8c4f60-76d5-422d-9d23-584e8eb5f1a1">ITfRange::GetEmbedded
      </a>



<a href="https://msdn.microsoft.com/fa53c1f1-50eb-45eb-b2ea-f236a376d41a">Miscellaneous Framework Constants</a>



<a href="https://msdn.microsoft.com/c827999a-0b74-4e5d-901e-4c2fa1d74929">Text Stores</a>
 

 

