---
UID: NF:vss.IVssEnumObject.Next
title: IVssEnumObject::Next
author: windows-driver-content
description: Returns the specified number of objects from the specified list of enumerated objects.
old-location: base\ivssenumobject_next.htm
old-project: VSS
ms.assetid: 9bfaba94-802f-47f5-9843-acc05b32f1b2
ms.author: windowsdriverdev
ms.date: 4/17/2018
ms.keywords: IVssEnumObject interface [VSS],Next method, IVssEnumObject.Next, IVssEnumObject::Next, Next, Next method [VSS], Next method [VSS],IVssEnumObject interface, _win32_ivssenumobject_next, base.ivssenumobject_next, vss/IVssEnumObject::Next
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: vss.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.typenames: VSS_WRITER_STATE, *PVSS_WRITER_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	VssApi.lib
-	VssApi.dll
api_name:
-	IVssEnumObject.Next
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVssEnumObject::Next


## -description


The 
<b>Next</b> method returns the specified number of objects from the specified list of enumerated objects.


## -parameters




### -param celt [in]

The number of elements to be read from the list of enumerated objects into the <i>rgelt</i> buffer.


### -param rgelt [out]

The address of a caller-allocated buffer that receives <i>celt</i><a href="https://msdn.microsoft.com/90664042-e9a0-4959-a975-9289477d2394">VSS_OBJECT_PROP</a> structures that contain the returned objects. This parameter is required and cannot be NULL.


### -param pceltFetched [out]

The number of elements that were returned in the <i>rgelt</i> buffer.


## -returns



The following are the valid return codes for this method.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The operation was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The number of returned items is less than the number requested.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
There is an internal error in the enumerator.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
One of the required pointer parameters is NULL.

</td>
</tr>
</table>
 




## -remarks



When requesting the return of more than one 
<a href="https://msdn.microsoft.com/90664042-e9a0-4959-a975-9289477d2394">VSS_OBJECT_PROP</a> object, a return value of S_FALSE indicates that the end of the enumeration list has been reached. If more objects were requested than remained in the list, 
<b>Next</b> will return all the remaining objects, set the <i>pceltFetched</i> parameter to a nonzero value, and return S_FALSE.

The output <i>rgelt</i> parameter must point to an allocated array containing <i>celt</i>
<a href="https://msdn.microsoft.com/90664042-e9a0-4959-a975-9289477d2394">VSS_OBJECT_PROP</a> structures, and cannot be NULL.

It is the caller's responsibility to free system resources returned by <b>IVssEnumObject::Next</b> to the 
<a href="https://msdn.microsoft.com/90664042-e9a0-4959-a975-9289477d2394">VSS_OBJECT_PROP</a> structure pointed to by the <i>rgelt</i> parameter.

The callers must use 
<a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a> for every string value in the 
<a href="https://msdn.microsoft.com/070ec204-e751-4ebf-8f99-3c415f203cb2">VSS_SNAPSHOT_PROP</a> or 
<a href="https://msdn.microsoft.com/000da95d-a3f5-447e-a96d-c8fb34e9d0d3">VSS_PROVIDER_PROP</a> object in the returned 
<a href="https://msdn.microsoft.com/90664042-e9a0-4959-a975-9289477d2394">VSS_OBJECT_PROP</a> structure.

In the case of 
<a href="https://msdn.microsoft.com/070ec204-e751-4ebf-8f99-3c415f203cb2">VSS_SNAPSHOT_PROP</a>, this can be done manually, or the utility function 
<a href="https://msdn.microsoft.com/d5b5883b-03d5-4a83-af2e-f4d22e26ee82">VssFreeSnapshotProperties</a> can be used.




## -see-also




<a href="https://msdn.microsoft.com/3f79bf84-c7b9-4291-ae3b-7061fe3199e9">IVssBackupComponents::Query</a>



<a href="https://msdn.microsoft.com/b8e80909-a28a-45d7-87e2-4f44bf6990f4">IVssEnumObject</a>



<a href="https://msdn.microsoft.com/90664042-e9a0-4959-a975-9289477d2394">VSS_OBJECT_PROP</a>
 

 

