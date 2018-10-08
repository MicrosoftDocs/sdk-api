---
UID: NF:oleidl.IOleObject.GetClipboardData
title: IOleObject::GetClipboardData
author: windows-sdk-content
description: Retrieves a data object containing the current contents of the embedded object on which this method is called. Using the pointer to this data object, it is possible to create a new embedded object with the same data as the original.
old-location: com\ioleobject_getclipboarddata.htm
tech.root: com
ms.assetid: 49f6b26c-76e1-4519-920b-e05279f23112
ms.author: windowssdkdev
ms.date: 10/02/2018
ms.keywords: GetClipboardData, GetClipboardData method [COM], GetClipboardData method [COM],IOleObject interface, IOleObject interface [COM],GetClipboardData method, IOleObject.GetClipboardData, IOleObject::GetClipboardData, _ole_ioleobject_getclipboarddata, com.ioleobject_getclipboarddata, oleidl/IOleObject::GetClipboardData
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: oleidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OleIdl.Idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OleIdl.h
api_name:
 - IOleObject.GetClipboardData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOleObject::GetClipboardData


## -description


Retrieves a data object containing the current contents of the embedded object on which this method is called. Using the pointer to this data object, it is possible to create a new embedded object with the same data as the original.


## -parameters




### -param dwReserved [in]

This parameter is reserved and must be zero.


### -param ppDataObject [out]

Address of <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a> pointer variable that receives the interface pointer to the data object. If an error occurs, <i>ppDataObject</i> must be set to <b>NULL</b>. Each time an object receives a call to <b>IOleObject::GetClipboardData</b>, it must increase the reference count on <i>ppDataObject</i>. It is the caller's responsibility to call <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a> when it is done with <i>ppDataObject</i>.


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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/49f6b26c-76e1-4519-920b-e05279f23112">GetClipboardData</a> is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLE_E_NOTRUNNING</b></dt>
</dl>
</td>
<td width="60%">
The object is not running.

</td>
</tr>
</table>
 




## -remarks



You can use the <b>IOleObject::GetClipboardData</b> method to convert a linked object to an embedded object, in which case the container application would call <b>IOleObject::GetClipboardData</b> and then pass the data received to <a href="https://msdn.microsoft.com/aa5e997e-60d4-472d-9c81-5359c277bde3">OleCreateFromData</a>. This method returns a pointer to a data object that is identical to what would have been passed to the clipboard by a standard copy operation.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
If you want a stable snapshot of the current contents of an embedded object, call <b>IOleObject::GetClipboardData</b>. Should the data change, you will need to call the function again for an updated snapshot. If you want the caller to be informed of changes that occur to the data, call <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a>, then call <a href="https://msdn.microsoft.com/be9891d4-aad3-42a0-8c8e-4b86091ff03b">IDataObject::DAdvise</a>.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
If you implement this function, you must return an <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a> pointer for an object whose data will not change.




## -see-also




<a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a>



<a href="https://msdn.microsoft.com/58b32c87-39b6-4d64-9174-cf798ed302c2">IOleObject</a>



<a href="https://msdn.microsoft.com/8bbda602-4421-4f79-a33a-63ded9a8bf90">IOleObject::InitFromData</a>



<a href="https://msdn.microsoft.com/aa5e997e-60d4-472d-9c81-5359c277bde3">OleCreateFromData</a>
 

 

