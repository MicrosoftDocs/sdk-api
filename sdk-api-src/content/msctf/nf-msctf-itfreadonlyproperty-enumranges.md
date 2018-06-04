---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# ITfReadOnlyProperty::EnumRanges


## -description




## -parameters




### -param ec [in]

Contains an edit cookie that identifies the edit context. This is obtained from <a href="https://msdn.microsoft.com/1415f338-731c-44c5-b798-edf823174272">ITfDocumentMgr::CreateContext</a> or <a href="https://msdn.microsoft.com/f89b2676-9a69-492f-be8a-96e4436d594c">ITfEditSession::DoEditSession</a>.


### -param ppEnum [out]

Pointer to an <a href="https://msdn.microsoft.com/68e17539-3b00-4e51-964d-0516b448f6c8">IEnumTfRanges</a> interface pointer that receives the enumerator object. The caller must release this object when it is no longer required.


### -param pTargetRange [in]

Pointer to an <a href="https://msdn.microsoft.com/b8889f7d-3228-4ecc-8d24-c04234d3101e">ITfRange</a> interface that specifies the range to scan for unique property values. This parameter is optional and can be <b>NULL</b>. For more information, see the Remarks section.


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
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred. 

<div class="alert"><b>Note</b>  If an application does not implement <a href="https://msdn.microsoft.com/f5917958-150e-48a5-9d0d-67240a88c232">ITextStoreACP::FindNextAttrTransition</a>, ITfReadOnlyProperty::EnumRanges fails with E_FAIL.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TF_E_NOLOCK</b></dt>
</dl>
</td>
<td width="60%">
The edit context identified by <i>ec</i> does not have a read-only or read/write lock.

</td>
</tr>
</table>
 




## -remarks



<b>Note:</b> If an application does not implement <a href="https://msdn.microsoft.com/f5917958-150e-48a5-9d0d-67240a88c232">ITextStoreACP::FindNextAttrTransition</a>, <b>ITfReadOnlyProperty::EnumRanges</b> fails with E_FAIL.

The enumerator obtained by this method will contain a range for each unique value, including empty values, of the specified property. For example, a hypothetical color property can be applied to the following marked up text:

<pre class="syntax" xml:space="preserve"><code>
COLOR:      RR      GGGGGGGG
TEXT:  this is some colored text
</code></pre>
When <b>ITfReadOnlyProperty::EnumRanges</b> is called with <i>pTargetRange</i> set to this range, the enumerator will contain five ranges.

<table>
<tr>
<th>Range Index</th>
<th>Color Property Value</th>
<th>Range Text</th>
</tr>
<tr>
<td>0</td>
<td>&lt;empty&gt;</td>
<td>"this "</td>
</tr>
<tr>
<td>1</td>
<td>R</td>
<td>"is"</td>
</tr>
<tr>
<td>2</td>
<td>&lt;empty&gt;</td>
<td>" some "</td>
</tr>
<tr>
<td>3</td>
<td>G</td>
<td>"colored "</td>
</tr>
<tr>
<td>4</td>
<td>&lt;empty&gt;</td>
<td>"text"</td>
</tr>
</table>
 

If <i>pTargetRange</i> is <b>NULL</b>, then the enumerator will begin and end with the first and last range that contains a non-empty property value in the context. Specifying <b>NULL</b> for <i>pTargetRange</i> in the above example would result in an enumerator with three ranges.

<table>
<tr>
<th>Range Index</th>
<th>Color Property Value</th>
<th>Text Within Range</th>
</tr>
<tr>
<td>0</td>
<td>R</td>
<td>"is"</td>
</tr>
<tr>
<td>1</td>
<td>&lt;empty&gt;</td>
<td>" some "</td>
</tr>
<tr>
<td>2</td>
<td>G</td>
<td>"colored "</td>
</tr>
</table>
 

The enumerated ranges will begin and end with the start and end anchors of <i>pTargetRange</i>, even if either anchor is positioned in the middle of a property.




## -see-also




<a href="https://msdn.microsoft.com/68e17539-3b00-4e51-964d-0516b448f6c8">
        IEnumTfRanges</a>



<a href="https://msdn.microsoft.com/1415f338-731c-44c5-b798-edf823174272">
        ITfDocumentMgr::CreateContext
      </a>



<a href="https://msdn.microsoft.com/f89b2676-9a69-492f-be8a-96e4436d594c">
        ITfEditSession::DoEditSession
      </a>



<a href="https://msdn.microsoft.com/b8889f7d-3228-4ecc-8d24-c04234d3101e">
        ITfRange</a>



<a href="https://msdn.microsoft.com/f4021a3d-6b86-469f-8943-770e7ef0cf99">ITfReadOnlyProperty</a>
 

 

