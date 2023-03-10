---
UID: NS:ntmsapi._NTMS_MEDIAPOOLINFORMATION
title: NTMS_MEDIAPOOLINFORMATION (ntmsapi.h)
description: The NTMS_MEDIAPOOLINFORMATION structure defines the properties specific to a media pool object.
helpviewer_keywords: ["NTMS_ALLOCATE_FROMSCRATCH","NTMS_DEALLOCATE_TOSCRATCH","NTMS_MEDIAPOOLINFORMATION","NTMS_MEDIAPOOLINFORMATION structure [Files]","NTMS_POOLTYPE_APPLICATION","NTMS_POOLTYPE_FOREIGN","NTMS_POOLTYPE_IMPORT","NTMS_POOLTYPE_SCRATCH","NTMS_POOLTYPE_UNKNOWN","_zaw_ntms_mediapoolinformation","base.ntms_mediapoolinformation","fs.ntms_mediapoolinformation","ntmsapi/NTMS_MEDIAPOOLINFORMATION"]
old-location: fs\ntms_mediapoolinformation.htm
tech.root: fs
ms.assetid: 4feb9d68-f88b-4515-9c59-64fe9c5594d6
ms.date: 12/05/2018
ms.keywords: NTMS_ALLOCATE_FROMSCRATCH, NTMS_DEALLOCATE_TOSCRATCH, NTMS_MEDIAPOOLINFORMATION, NTMS_MEDIAPOOLINFORMATION structure [Files], NTMS_POOLTYPE_APPLICATION, NTMS_POOLTYPE_FOREIGN, NTMS_POOLTYPE_IMPORT, NTMS_POOLTYPE_SCRATCH, NTMS_POOLTYPE_UNKNOWN, _zaw_ntms_mediapoolinformation, base.ntms_mediapoolinformation, fs.ntms_mediapoolinformation, ntmsapi/NTMS_MEDIAPOOLINFORMATION
req.header: ntmsapi.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: NTMS_MEDIAPOOLINFORMATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _NTMS_MEDIAPOOLINFORMATION
 - ntmsapi/_NTMS_MEDIAPOOLINFORMATION
 - NTMS_MEDIAPOOLINFORMATION
 - ntmsapi/NTMS_MEDIAPOOLINFORMATION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntmsapi.h
api_name:
 - NTMS_MEDIAPOOLINFORMATION
---

# NTMS_MEDIAPOOLINFORMATION structure


## -description

<p class="CCE_Message">[<a href="/previous-versions/windows/desktop/bb540725(v=vs.85)">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>NTMS_MEDIAPOOLINFORMATION</b> structure defines the properties specific to a media pool object.

## -struct-fields

### -field PoolType

NTMS supports the following media pool types. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NTMS_POOLTYPE_UNKNOWN"></a><a id="ntms_pooltype_unknown"></a><dl>
<dt><b>NTMS_POOLTYPE_UNKNOWN</b></dt>
</dl>
</td>
<td width="60%">
Unknown pool type.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_POOLTYPE_SCRATCH"></a><a id="ntms_pooltype_scratch"></a><dl>
<dt><b>NTMS_POOLTYPE_SCRATCH</b></dt>
</dl>
</td>
<td width="60%">
Media that is available to other applications.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_POOLTYPE_FOREIGN"></a><a id="ntms_pooltype_foreign"></a><dl>
<dt><b>NTMS_POOLTYPE_FOREIGN</b></dt>
</dl>
</td>
<td width="60%">
Media that has been written to and does not contain a recognizable on-media identifier label-type or label ID.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_POOLTYPE_IMPORT"></a><a id="ntms_pooltype_import"></a><dl>
<dt><b>NTMS_POOLTYPE_IMPORT</b></dt>
</dl>
</td>
<td width="60%">
Media that has been written to, has a recognizable on-media identifier label type but an unrecognizable label ID.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_POOLTYPE_APPLICATION"></a><a id="ntms_pooltype_application"></a><dl>
<dt><b>NTMS_POOLTYPE_APPLICATION</b></dt>
</dl>
</td>
<td width="60%">
Media pool created by an application. One or more application media pools can be created per system.

</td>
</tr>
</table>

### -field MediaType

Single media type that makes up each media pool.

### -field Parent

Parent media pool or <b>NULL</b>.

### -field AllocationPolicy

Bit field indicating action at allocation time. This member is writable. This can be the following value. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NTMS_ALLOCATE_FROMSCRATCH"></a><a id="ntms_allocate_fromscratch"></a><dl>
<dt><b>NTMS_ALLOCATE_FROMSCRATCH</b></dt>
</dl>
</td>
<td width="60%">
Draw media from free if none is available in the pool. The default is not to draw from free.

</td>
</tr>
</table>

### -field DeallocationPolicy

Bit field indicating action at deallocation time. This member is writable. This can be the following value. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NTMS_DEALLOCATE_TOSCRATCH"></a><a id="ntms_deallocate_toscratch"></a><dl>
<dt><b>NTMS_DEALLOCATE_TOSCRATCH</b></dt>
</dl>
</td>
<td width="60%">
Return media to free when available. The default is not to return to free.

</td>
</tr>
</table>

### -field dwMaxAllocates

Number of times the medium can be allocated and deallocated. This member is writable.

### -field dwNumberOfPhysicalMedia

Number of physical media in this media pool.

### -field dwNumberOfLogicalMedia

Number of logical media in this media pool.

### -field dwNumberOfMediaPools

Number of media pools in this media pool.

## -remarks

The 
<b>NTMS_MEDIAPOOLINFORMATION</b> structure is included in the 
<a href="/windows/desktop/api/ntmsapi/ns-ntmsapi-ntms_objectinformationa">NTMS_OBJECTINFORMATION</a> structure.

## -see-also

<a href="/windows/desktop/api/ntmsapi/ns-ntmsapi-ntms_objectinformationa">NTMS_OBJECTINFORMATION</a>