---
UID: NF:msctf.ITfRange.AdjustForInsert
title: ITfRange::AdjustForInsert method
author: windows-driver-content
description: The ITfRange::AdjustForInsert method expands or contracts a range of text to adjust for text insertion.
old-location: tsf\itfrange_adjustforinsert.htm
old-project: TSF
ms.assetid: b286266c-d6cf-4291-b4b2-24d5a3d4e1ad
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: AdjustForInsert method [Text Services Framework], AdjustForInsert method [Text Services Framework], ITfRange interface, AdjustForInsert,ITfRange.AdjustForInsert, ITfRange, ITfRange interface [Text Services Framework], AdjustForInsert method, ITfRange::AdjustForInsert, _tsf_itfrange_adjustforinsert_ref, msctf/ITfRange::AdjustForInsert, tsf.itfrange_adjustforinsert
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TF_DA_ATTR_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Msctf.dll
api_name:
-	ITfRange.AdjustForInsert
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfRange::AdjustForInsert method


## -description


The <b>ITfRange::AdjustForInsert</b> method expands or contracts a range of text to adjust for text insertion.


## -parameters




### -param ec [in]

Edit cookie obtained from <a href="https://msdn.microsoft.com/1415f338-731c-44c5-b798-edf823174272">ITfDocumentMgr::CreateContext</a> or <a href="https://msdn.microsoft.com/f89b2676-9a69-492f-be8a-96e4436d594c">ITfEditSession::DoEditSession</a>.


### -param cchInsert [in]

Character count of the inserted text. This count is used in a futurecall to <a href="https://msdn.microsoft.com/797d96a1-0250-4e8d-a4bd-31152fd6eca7">ITfRange::SetText</a>. If the character count is unknown, 0 can be used.


### -param pfInsertOk [out]

Pointer to a flag that indicates whether the context owner will accept (<b>TRUE</b>) or reject (<b>FALSE</b>) the insertion.


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
The method failed.

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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The application was unable to replace the selection.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TF_E_NOLOCK</b></dt>
</dl>
</td>
<td width="60%">
The value in the <i>ec</i> parameter is an invalid cookie, or the caller does not have a read-only lock.

</td>
</tr>
</table>
 




## -remarks



This method should be used to prepare a range to initiate a new composition, before editing begins. It should be used only when the text is not inserted at the current selection. <a href="https://msdn.microsoft.com/1373fe9b-6c51-4514-a7da-c1f872d9b1ce">ITFInsertAtSelection:InsertTextAtSelection</a> or <a href="https://msdn.microsoft.com/13fa9955-0087-4dd9-8a1d-814ab801e956">ITfInsertAtSelection::InsertEmbeddedAtSelection</a> are the correct methods to use when text is inserted at the current selection.

The context owner can use this method to preserve behavior and help maintain a consistent user experience. For example, certain characters or objects in the context can be preserved from modifications, or overtyping can be supported.

This method is not necessary when modifying an existing composition. It is acceptable to call <b>ITfRange::SetText</b> directly to modify text previously entered by the caller.

On exit, if <i>*pfInsertOk</i> is set to <b>FALSE</b>, a future call to <b>ITfRange::SetText</b> or <a href="https://msdn.microsoft.com/95b8622d-c934-4293-abb4-9eface451be5">ITfRange::InsertEmbedded</a> with this range is likely to fail. Otherwise, <i>*pfInsertOk</i> will be set to <b>TRUE</b>, and the range start anchor or end anchor can be repositioned at the discretion of the context owner.




## -see-also




<a href="https://msdn.microsoft.com/1373fe9b-6c51-4514-a7da-c1f872d9b1ce">
        ITFInsertAtSelection:InsertTextAtSelection
      </a>



<a href="https://msdn.microsoft.com/1415f338-731c-44c5-b798-edf823174272">ITfDocumentMgr::CreateContext
      </a>



<a href="https://msdn.microsoft.com/f89b2676-9a69-492f-be8a-96e4436d594c">
        ITfEditSession::DoEditSession
      </a>



<a href="https://msdn.microsoft.com/13fa9955-0087-4dd9-8a1d-814ab801e956">
        ITfInsertAtSelection::InsertEmbeddedAtSelection
      </a>



<a href="https://msdn.microsoft.com/b8889f7d-3228-4ecc-8d24-c04234d3101e">ITfRange</a>



<a href="https://msdn.microsoft.com/95b8622d-c934-4293-abb4-9eface451be5">
        ITfRange::InsertEmbedded
      </a>



<a href="https://msdn.microsoft.com/797d96a1-0250-4e8d-a4bd-31152fd6eca7">
        ITfRange::SetText
      </a>



<a href="https://msdn.microsoft.com/c827999a-0b74-4e5d-901e-4c2fa1d74929">Text Stores</a>
 

 

