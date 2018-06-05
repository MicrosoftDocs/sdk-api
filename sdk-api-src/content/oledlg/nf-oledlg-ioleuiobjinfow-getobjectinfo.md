---
UID: NF:oledlg.IOleUIObjInfoW.GetObjectInfo
title: IOleUIObjInfoW::GetObjectInfo
author: windows-sdk-content
description: Gets the size, type, name, and location information for an object.
old-location: com\ioleuiobjinfo_getobjectinfo.htm
old-project: com
ms.assetid: d09aafd0-0f4b-42c4-b1e6-0656cf0bd02d
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: GetObjectInfo, GetObjectInfo method [COM], GetObjectInfo method [COM],IOleUIObjInfo interface, GetObjectInfo method [COM],IOleUIObjInfoA interface, GetObjectInfo method [COM],IOleUIObjInfoW interface, IOleUIObjInfo interface [COM],GetObjectInfo method, IOleUIObjInfo::GetObjectInfo, IOleUIObjInfoA interface [COM],GetObjectInfo method, IOleUIObjInfoA::GetObjectInfo, IOleUIObjInfoW interface [COM],GetObjectInfo method, IOleUIObjInfoW.GetObjectInfo, IOleUIObjInfoW::GetObjectInfo, _ole_IOleUIObjInfo_GetObjectInfo, com.ioleuiobjinfo_getobjectinfo, oledlg/IOleUIObjInfo::GetObjectInfo, oledlg/IOleUIObjInfoA::GetObjectInfo, oledlg/IOleUIObjInfoW::GetObjectInfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: oledlg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: OLEUIPASTEFLAG
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	OleDlg.h
api_name:
-	IOleUIObjInfo.GetObjectInfo
-	IOleUIObjInfoW.GetObjectInfo
-	IOleUIObjInfoA.GetObjectInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IOleUIObjInfoW::GetObjectInfo


## -description


Gets the size, type, name, and location information for an object.


## -parameters




### -param dwObject [in]

Unique identifier for the object.


### -param lpdwObjSize [out]

Pointer to the object's size, in bytes, on disk. This may be an approximate value.


### -param lplpszLabel [out, optional]

Address of a pointer variable that receives a pointer to the object's label string. This parameter may be <b>NULL</b> to indicate that the implementation should not return the label string.


### -param lplpszType [out, optional]

Address of a pointer variable that receives a pointer to the object's long type string. This parameter may be <b>NULL</b> to indicate that the implementation should not return the long type string.


### -param lplpszShortType [out, optional]

Address of a pointer variable that receives a pointer to the object's short type string. This parameter may be <b>NULL</b> to indicate that the implementation should not return the short type string.


### -param lplpszLocation [out, optional]

Address of a pointer variable that receives a pointer to the object's source location string. This parameter may be <b>NULL</b> to indicate that the implementation should not return the location string.


## -returns



This method returns S_OK on success. Other possible return values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The operation failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The specified identifier is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is insufficient memory available for this operation.

</td>
</tr>
</table>
 




## -remarks



The strings and the object's size are displayed in the object properties <b>General</b> page.


<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
Your implementation of <b>GetObjectInfo</b> should place each of the object's attributes in the out parameters provided. Set <i>lpdwObjSize</i> to (DWORD)-1 when the size of the object is unknown. Allocate all strings (the rest of the params) with the OLE task allocator obtained via <a href="https://msdn.microsoft.com/d1d09fbe-ca5c-4480-b807-3afcc043ccb9">CoGetMalloc</a>, as is standard for all OLE interfaces with [out] string parameters, or you can simply use <a href="https://msdn.microsoft.com/c4cb588d-9482-4f90-a92e-75b604540d5c">CoTaskMemAlloc</a>.




## -see-also




<a href="https://msdn.microsoft.com/d1d09fbe-ca5c-4480-b807-3afcc043ccb9">CoGetMalloc</a>



<a href="https://msdn.microsoft.com/c4cb588d-9482-4f90-a92e-75b604540d5c">CoTaskMemAlloc</a>



<a href="https://msdn.microsoft.com/508dccb3-e98b-4f62-8bc3-98ca2b0d1349">IOleUIObjInfo</a>
 

 

