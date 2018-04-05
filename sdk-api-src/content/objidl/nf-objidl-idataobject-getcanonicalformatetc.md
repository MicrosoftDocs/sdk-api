---
UID: NF:objidl.IDataObject.GetCanonicalFormatEtc
title: IDataObject::GetCanonicalFormatEtc method
author: windows-driver-content
description: Provides a potentially different but logically equivalent FORMATETC structure. You use this method to determine whether two different FORMATETC structures would return the same data, removing the need for duplicate rendering.
old-location: com\idataobject_getcanonicalformatetc.htm
old-project: com
ms.assetid: 3a5009a0-8d92-483a-b055-8a97f326dccd
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: GetCanonicalFormatEtc method [COM], GetCanonicalFormatEtc method [COM], IDataObject interface, GetCanonicalFormatEtc,IDataObject.GetCanonicalFormatEtc, IDataObject, IDataObject interface [COM], GetCanonicalFormatEtc method, IDataObject::GetCanonicalFormatEtc, _ole_idataobject_getcanonicalformatetc, com.idataobject_getcanonicalformatetc, objidl/IDataObject::GetCanonicalFormatEtc
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: THDTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ObjIdl.h
api_name:
-	IDataObject.GetCanonicalFormatEtc
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IDataObject::GetCanonicalFormatEtc method


## -description


Provides a potentially different but logically equivalent <a href="https://msdn.microsoft.com/4478eb9a-84a1-4f3a-8290-94b8dd20c081">FORMATETC</a> structure. You use this method to determine whether two different <b>FORMATETC</b> structures would return the same data, removing the need for duplicate rendering.


## -parameters




### -param pformatectIn [in]

A pointer to the <a href="https://msdn.microsoft.com/4478eb9a-84a1-4f3a-8290-94b8dd20c081">FORMATETC</a> structure that defines the format, medium, and target device that the caller would like to use to retrieve data in a subsequent call such as <a href="https://msdn.microsoft.com/05118461-0438-4715-b2c2-fc2471ce38f0">IDataObject::GetData</a>. The <b>tymed</b> member is not significant in this case and should be ignored.


### -param pformatetcOut [out]

A pointer to a <a href="https://msdn.microsoft.com/4478eb9a-84a1-4f3a-8290-94b8dd20c081">FORMATETC</a> structure that contains the most general information possible for a specific rendering, making it canonically equivalent to <i>pformatetcIn</i>. The caller must allocate this structure and the <b>GetCanonicalFormatEtc</b> method must fill in the data. To retrieve data in a subsequent call like <a href="https://msdn.microsoft.com/05118461-0438-4715-b2c2-fc2471ce38f0">IDataObject::GetData</a>, the caller uses the specified value of <i>pformatetcOut</i>, unless the value specified is <b>NULL</b>. This value is <b>NULL</b> if the method returns DATA_S_SAMEFORMATETC. The <b>tymed</b> member is not significant in this case and should be ignored.


## -returns



This method can return the following values.

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
The returned <a href="https://msdn.microsoft.com/4478eb9a-84a1-4f3a-8290-94b8dd20c081">FORMATETC</a> structure is different from the one that was passed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DATA_S_SAMEFORMATETC</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/4478eb9a-84a1-4f3a-8290-94b8dd20c081">FORMATETC</a> structures are the same and <b>NULL</b> is returned in <i>pformatetcOut</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DV_E_LINDEX</b></dt>
</dl>
</td>
<td width="60%">
The value for <b>lindex</b> is not valid; currently, only -1 is supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DV_E_FORMATETC</b></dt>
</dl>
</td>
<td width="60%">
The value for <i>pformatetc</i> is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLE_E_NOTRUNNING</b></dt>
</dl>
</td>
<td width="60%">
The object application is not running.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
An unexpected error has occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwDirection</i> parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There was insufficient memory available for this operation.

</td>
</tr>
</table>
 




## -remarks



If a data object can supply exactly the same data for more than one requested <a href="https://msdn.microsoft.com/4478eb9a-84a1-4f3a-8290-94b8dd20c081">FORMATETC</a> structure, <b>GetCanonicalFormatEtc</b> can supply a "canonical", or standard <b>FORMATETC</b> that gives the same rendering as a set of more complicated <b>FORMATETC</b> structures. For example, it is common for the data returned to be insensitive to the target device specified in any one of a set of otherwise similar <b>FORMATETC</b> structures.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
A call to this method can determine whether two calls to <a href="https://msdn.microsoft.com/05118461-0438-4715-b2c2-fc2471ce38f0">IDataObject::GetData</a> on a data object, specifying two different <a href="https://msdn.microsoft.com/4478eb9a-84a1-4f3a-8290-94b8dd20c081">FORMATETC</a> structures, would actually produce the same renderings, thus eliminating the need for the second call and improving performance. If the call to <b>GetCanonicalFormatEtc</b> results in a canonical format being written to the <i>pformatetcOut</i> parameter, the caller then uses that structure in a subsequent call to <b>IDataObject::GetData</b>.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
Conceptually, it is possible to think of <a href="https://msdn.microsoft.com/4478eb9a-84a1-4f3a-8290-94b8dd20c081">FORMATETC</a> structures in groups defined by a canonical <b>FORMATETC</b> that provides the same results as each of the group members. In constructing the canonical <b>FORMATETC</b>, you should make sure it contains the most general information possible that still produces a specific rendering.

For data objects that never provide device-specific renderings, the simplest implementation of this method is to copy the input <a href="https://msdn.microsoft.com/4478eb9a-84a1-4f3a-8290-94b8dd20c081">FORMATETC</a> to the output <b>FORMATETC</b>, store a <b>NULL</b> in the <b>ptd</b> member of the output <b>FORMATETC</b>, and return DATA_S_SAMEFORMATETC.




## -see-also




<a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a>
 

 

