---
UID: NF:msctf.ITfContext.GetSelection
title: ITfContext::GetSelection method
author: windows-driver-content
description: ITfContext::GetSelection method
old-location: tsf\itfcontext_getselection.htm
old-project: TSF
ms.assetid: 08b67fd5-aebe-49f7-af78-6f49c8f47f64
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: GetSelection method [Text Services Framework], GetSelection method [Text Services Framework], ITfContext interface, GetSelection,ITfContext.GetSelection, ITfContext, ITfContext interface [Text Services Framework], GetSelection method, ITfContext::GetSelection, _tsf_itfcontext_getselection_ref, msctf/ITfContext::GetSelection, tsf.itfcontext_getselection
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
-	msctf.dll
api_name:
-	ITfContext.GetSelection
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfContext::GetSelection method


## -description




## -parameters




### -param ec [in]

Contains an edit cookie that identifies the edit session. This is the value passed to <a href="https://msdn.microsoft.com/f89b2676-9a69-492f-be8a-96e4436d594c">ITfEditSession::DoEditSession</a>.


### -param ulIndex [in]

Specifies the zero-based index of the first selection to obtain. Use TF_DEFAULT_SELECTION to obtain the default selection. If TF_DEFAULT_SELECTION is used, only one selection is obtained.


### -param ulCount [in]

Specifies the maximum number of selections to obtain.


### -param pSelection [out]

An array of <a href="https://msdn.microsoft.com/c844a6d1-b3b9-49cf-83a6-1ee8b3bd2d54">TF_SELECTION</a> structures that receives the data for each selection. The array must be able to hold at least <i>ulCount</i> elements.


### -param pcFetched [out]

Pointer to a ULONG value that receives the number of selections obtained.


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
<dt><b>TF_E_NOSELECTION</b></dt>
</dl>
</td>
<td width="60%">
The document has no selection.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TF_E_NOLOCK</b></dt>
</dl>
</td>
<td width="60%">
The cookie in <i>ec</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TF_E_DISCONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The context is not on a document stack.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation failure occurred.

</td>
</tr>
</table>
 




## -remarks



A selection is a highlighted range of text, or an insertion point if the range is empty, that identifies the user focus area within a document.

If this method is successful, the caller must release the <b>range</b> member of all <b>TF_SELECTION</b> structures obtained.

Normally, a context only supports a single selection. It is possible, however, for a context to support multiple, simultaneous selections. This method can be used to obtain multiple selections.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
HRESULT         hr;
TF_SELECTION    tfSel;
ULONG           uFetched;

//Obtain the default selection. 
hr = pContext-&gt;GetSelection(ec, TF_DEFAULT_SELECTION, 1, &amp;tfSel, &amp;uFetched);
if(SUCCEEDED(hr) &amp;&amp; (uFetched &gt; 0))
{
    //Work with the selection. 
    
    //Release the selection range object. 
    tfSel.range-&gt;Release();
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/ca98c7bb-7348-405d-976a-18012b0886c6">ITfContext</a>



<a href="https://msdn.microsoft.com/f89b2676-9a69-492f-be8a-96e4436d594c">ITfEditSession::DoEditSession
      </a>



<a href="https://msdn.microsoft.com/c844a6d1-b3b9-49cf-83a6-1ee8b3bd2d54">
        TF_SELECTION
      </a>
 

 

