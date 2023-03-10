---
UID: NF:vss.IVssEnumObject.Next
title: IVssEnumObject::Next (vss.h)
description: Returns the specified number of objects from the specified list of enumerated objects. (IVssEnumObject.Next)
helpviewer_keywords: ["IVssEnumObject interface [VSS]","Next method","IVssEnumObject.Next","IVssEnumObject::Next","Next","Next method [VSS]","Next method [VSS]","IVssEnumObject interface","_win32_ivssenumobject_next","base.ivssenumobject_next","vss/IVssEnumObject::Next"]
old-location: base\ivssenumobject_next.htm
tech.root: base
ms.assetid: 9bfaba94-802f-47f5-9843-acc05b32f1b2
ms.date: 12/05/2018
ms.keywords: IVssEnumObject interface [VSS],Next method, IVssEnumObject.Next, IVssEnumObject::Next, Next, Next method [VSS], Next method [VSS],IVssEnumObject interface, _win32_ivssenumobject_next, base.ivssenumobject_next, vss/IVssEnumObject::Next
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
req.lib: VssApi.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVssEnumObject::Next
 - vss/IVssEnumObject::Next
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VssApi.lib
 - VssApi.dll
api_name:
 - IVssEnumObject.Next
---

# IVssEnumObject::Next


## -description

The 
<b>Next</b> method returns the specified number of objects from the specified list of enumerated objects.

## -parameters

### -param celt [in]

The number of elements to be read from the list of enumerated objects into the <i>rgelt</i> buffer.

### -param rgelt [out]

The address of a caller-allocated buffer that receives <i>celt</i><a href="/windows/desktop/api/vss/ns-vss-vss_object_prop">VSS_OBJECT_PROP</a> structures that contain the returned objects. This parameter is required and cannot be NULL.

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
<a href="/windows/desktop/api/vss/ns-vss-vss_object_prop">VSS_OBJECT_PROP</a> object, a return value of S_FALSE indicates that the end of the enumeration list has been reached. If more objects were requested than remained in the list, 
<b>Next</b> will return all the remaining objects, set the <i>pceltFetched</i> parameter to a nonzero value, and return S_FALSE.

The output <i>rgelt</i> parameter must point to an allocated array containing <i>celt</i>
<a href="/windows/desktop/api/vss/ns-vss-vss_object_prop">VSS_OBJECT_PROP</a> structures, and cannot be NULL.

It is the caller's responsibility to free system resources returned by <b>IVssEnumObject::Next</b> to the 
<a href="/windows/desktop/api/vss/ns-vss-vss_object_prop">VSS_OBJECT_PROP</a> structure pointed to by the <i>rgelt</i> parameter.

The callers must use 
<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> for every string value in the 
<a href="/windows/desktop/api/vss/ns-vss-vss_snapshot_prop">VSS_SNAPSHOT_PROP</a> or 
<a href="/windows/desktop/api/vss/ns-vss-vss_provider_prop">VSS_PROVIDER_PROP</a> object in the returned 
<a href="/windows/desktop/api/vss/ns-vss-vss_object_prop">VSS_OBJECT_PROP</a> structure.

In the case of 
<a href="/windows/desktop/api/vss/ns-vss-vss_snapshot_prop">VSS_SNAPSHOT_PROP</a>, this can be done manually, or the utility function 
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-vssfreesnapshotproperties">VssFreeSnapshotProperties</a> can be used.

## -see-also

<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-query">IVssBackupComponents::Query</a>



<a href="/windows/desktop/api/vss/nn-vss-ivssenumobject">IVssEnumObject</a>



<a href="/windows/desktop/api/vss/ns-vss-vss_object_prop">VSS_OBJECT_PROP</a>
