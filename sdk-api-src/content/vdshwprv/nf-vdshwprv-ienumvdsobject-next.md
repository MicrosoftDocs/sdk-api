---
UID: NF:vdshwprv.IEnumVdsObject.Next
title: IEnumVdsObject::Next
author: windows-sdk-content
description: Returns a specified number of objects in the enumeration, beginning from the current point. For more information, see Working with Enumeration Objects.
old-location: base\ienumvdsobject_next.htm
old-project: VDS
ms.assetid: 372eff29-7481-45aa-ad66-73147f7a631f
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: IEnumVdsObject interface [VDS],Next method, IEnumVdsObject.Next, IEnumVdsObject::Next, Next, Next method [VDS], Next method [VDS],IEnumVdsObject interface, base.ienumvdsobject_next, vds/IEnumVdsObject::Next, vdshwprv/IEnumVdsObject::Next
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: vdshwprv.h
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
tech.root: 
req.typenames: VDS_VERSION_SUPPORT_FLAG
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uuid.lib
 - Uuid.dll
api_name:
 - IEnumVdsObject.Next
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IEnumVdsObject::Next


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Returns a specified number of 
   objects in the enumeration, beginning from the current point. For more information, see <a href="https://msdn.microsoft.com/cb99e9fd-613c-4e38-9e0f-e1a23b72aa07">Working with Enumeration Objects</a>.


## -parameters




### -param celt [in]

The number of objects to return.


### -param ppObjectArray [out]

The address of an array of <a href="_com_iunknown">IUnknown</a> pointers, which VDS initializes 
      on return.


### -param pcFetched [out]

The address of a <b>ULONG</b>, which VDS initializes on return to the number of 
      objects in <i>ppObjectArray</i>.


## -returns



This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="https://msdn.microsoft.com/c9ddd3b7-f017-4880-976a-c879a40dc17b">VDS-specific return values</a>. It can also return converted <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>  using the <a href="_com_hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="https://msdn.microsoft.com/b2f7628c-b567-40a9-9ad7-6c47077af5fb">VDS provider</a> that is being used. Possible return values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method returned the specified number of objects. The number of returned objects reported in 
        <i>pcFetched</i> equals <i>celt</i>; returns those objects.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The specified number of returned objects is greater than the number of objects remaining. All remaining 
        objects are returned, and the number of returned objects is reported in <i>pcFetched</i> is 
        less than <i>celt</i>; returns those objects.

</td>
</tr>
</table>
 




## -remarks



To obtain object-specific interface pointers from the <a href="_com_iunknown">IUnknown</a> pointers returned in the <i>ppObjectArray</i> array, use the <a href="_com_iunknown_queryinterface">IUnknown::QueryInterface</a> method.




## -see-also




<a href="https://msdn.microsoft.com/08379071-b3cc-495a-bc8e-ad6cfacd432c">IEnumVdsObject</a>
 

 

