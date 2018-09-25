---
UID: NF:oleidl.IOleObject.IsUpToDate
title: IOleObject::IsUpToDate
author: windows-sdk-content
description: Checks whether an object is up to date.
old-location: com\ioleobject_isuptodate.htm
tech.root: com
ms.assetid: 74203a74-c5dd-4a98-9223-1dc54c9d4399
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: IOleObject interface [COM],IsUpToDate method, IOleObject.IsUpToDate, IOleObject::IsUpToDate, IsUpToDate, IsUpToDate method [COM], IsUpToDate method [COM],IOleObject interface, _ole_ioleobject_isuptodate, com.ioleobject_isuptodate, oleidl/IOleObject::IsUpToDate
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
 - IOleObject.IsUpToDate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOleObject::IsUpToDate


## -description


Checks whether an object is up to date.


## -parameters






## -returns



This method returns S_OK if the object is up to date; otherwise, S_FALSE. Other possible return values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLE_E_UNAVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
The status of object cannot be determined in a timely manner.

</td>
</tr>
</table>
 




## -remarks



The <b>IOleObject::IsUpToDate</b> method provides a way for containers to check recursively whether all objects are up to date. That is, when the container calls this method on the first object, the object in turn calls it for all its own objects, and they in turn for all of theirs, until all objects have been checked.


<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
Because of the recursive nature of <b>IOleObject::IsUpToDate</b>, determining whether an object is out-of-date, particularly one containing one or more other objects, can be as time-consuming as simply updating the object in the first place. If you would rather avoid lengthy queries of this type, make sure that <b>IOleObject::IsUpToDate</b> returns OLE_E_UNAVAILABLE. In cases where the object to be queried is small and contains no objects itself, thereby making an efficient query possible, this method can return either S_OK or S_FALSE.




## -see-also




<a href="https://msdn.microsoft.com/58b32c87-39b6-4d64-9174-cf798ed302c2">IOleObject</a>



<a href="https://msdn.microsoft.com/1743f99b-4c3b-47be-b77b-1d3378a44903">IOleObject::Update</a>
 

 

