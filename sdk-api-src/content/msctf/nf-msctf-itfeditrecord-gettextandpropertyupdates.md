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

# ITfEditRecord::GetTextAndPropertyUpdates


## -description




## -parameters




### -param dwFlags [in]

Contains a combination of the following values that specify the behavior of this method.

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
Specifies that the method will obtain a collection of range objects that cover the specified properties changed during the edit session. <i>prgProperties</i> cannot be <b>NULL</b> and <i>cProperties</i> must be greater than zero.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_GTP_INCL_TEXT"></a><a id="tf_gtp_incl_text"></a><dl>
<dt><b>TF_GTP_INCL_TEXT</b></dt>
</dl>
</td>
<td width="60%">
Specifies that the method will obtain the collection of range objects that cover the text changed during the edit session.

</td>
</tr>
</table>
 


### -param prgProperties [in]

Pointer to an array of <b>GUID</b> values that identify the properties to search for changes for. This method searches the properties that changed during the edit session and, if the property is contained in this array, a range object that covers the property that changed is added to <i>ppEnum</i>.

This array must be at least <i>cProperties</i> elements in size.

This parameter is ignored if <i>dwFlags</i> contains TF_GTP_INCL_TEXT and <i>cProperties</i> is zero.


### -param cProperties [in]

Specifies the number of elements in the <i>prgProperties</i> array.

This parameter can be zero if <i>dwFlags</i> contains TF_GTP_INCL_TEXT. This indicates that no property changes are obtained.


### -param ppEnum [out]

Pointer to an <a href="https://msdn.microsoft.com/68e17539-3b00-4e51-964d-0516b448f6c8">IEnumTfRanges</a> interface pointer that receives the enumerator object.


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
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/68e17539-3b00-4e51-964d-0516b448f6c8">IEnumTfRanges
      </a>



<a href="https://msdn.microsoft.com/2106cd97-9e1f-4d7c-a7a4-55676cf8923b">ITfEditRecord</a>
 

 

