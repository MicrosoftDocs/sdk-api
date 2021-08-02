---
UID: NF:fltuser.FilterAttach
title: FilterAttach function (fltuser.h)
description: The FilterAttach function attaches a new minifilter instance to the given volume.
helpviewer_keywords: ["FilterAttach","FilterAttach function [Installable File System Drivers]","FltWin32ApiRef_023a1285-b933-438f-b493-33e6c7d74e56.xml","fltuser/FilterAttach","ifsk.filterattach"]
old-location: ifsk\filterattach.htm
tech.root: ifsk
ms.assetid: 8f52fdd5-dfea-42c1-85ed-7431015eece8
ms.date: 12/05/2018
ms.keywords: FilterAttach, FilterAttach function [Installable File System Drivers], FltWin32ApiRef_023a1285-b933-438f-b493-33e6c7d74e56.xml, fltuser/FilterAttach, ifsk.filterattach
req.header: fltuser.h
req.include-header: Fltuser.h
req.target-type: Universal
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
req.lib: FltLib.lib
req.dll: FltLib.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FilterAttach
 - fltuser/FilterAttach
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - FltLib.dll
api_name:
 - FilterAttach
---

# FilterAttach function


## -description

The <b>FilterAttach</b> function attaches a new minifilter instance to the given volume.

## -parameters

### -param lpFilterName [in]

Pointer to a null-terminated wide-character string containing the name of the minifilter for which an instance is to be created. This parameter is required and cannot be <b>NULL</b>.

### -param lpVolumeName [in]

Pointer to a null-terminated wide-character string containing the name of the volume to which the newly created instance is to be attached. 

The <i>lpVolumeName</i> input string can be any of the following. The trailing backslash (\\) is optional. 

<ul>
<li>
A drive letter, such as "D:\"

</li>
<li>
A path to a volume mount point, such as "c:\mnt\edrive\"

</li>
<li>
A unique volume identifier (also called a <i>volume GUID name</i>), such as "\??\Volume{7603f260-142a-11d4-ac67-806d6172696f}\"

</li>
<li>
A nonpersistent device name (also called a <i>target name</i> or an <i>NT device name</i>), such as "\Device\HarddiskVolume1\"

</li>
</ul>
The <i>lpVolumeName</i> parameter is required and cannot be <b>NULL</b>.

### -param lpInstanceName [in, optional]

Pointer to a null-terminated wide-character string containing the instance name for the new instance. This parameter is optional and can be <b>NULL</b>. If this parameter is <b>NULL</b>, the new instance receives the minifilter's default instance name as described in the Remarks section for <a href="/windows-hardware/drivers/ddi/content/fltkernel/nf-fltkernel-fltattachvolume">FltAttachVolume</a>.

### -param dwCreatedInstanceNameLength [in, optional]

Length, in bytes, of the buffer that <i>lpCreatedInstanceName </i> points to. This parameter is optional and can be zero.

### -param lpCreatedInstanceName [out, optional]

Pointer to a caller-allocated variable that receives the instance name for the new instance if the instance is successfully attached to the volume. This parameter is optional and can be <b>NULL</b>. If it is not <b>NULL</b>, the buffer must be large enough to hold INSTANCE_NAME_MAX_CHARS characters plus a NULL terminator.

## -returns

<b>FilterAttach</b> returns S_OK if successful. Otherwise, it returns an error value such as one of the following. 

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FLT_INSTANCE_ALTITUDE_COLLISION</b></dt>
</dl>
</td>
<td width="60%">
An instance already exists at this altitude on the volume specified. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FLT_INSTANCE_NAME_COLLISION</b></dt>
</dl>
</td>
<td width="60%">
An instance already exists with this name on the volume specified. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
If <i>lpInstanceName</i> is non-<b>NULL</b>, <i>lpInstanceName</i> does not match a registered filter instance name in the registry.

</td>
</tr>
</table>

## -remarks

<b>FilterAttach</b> is the Win32 equivalent of <a href="/windows-hardware/drivers/ddi/content/fltkernel/nf-fltkernel-fltattachvolume">FltAttachVolume</a>. 

The instance name specified in <i>lpInstanceName</i> is required to be unique across the system. 

To attach a minifilter instance to a volume at a given altitude, call <a href="/windows/desktop/api/fltuser/nf-fltuser-filterattachataltitude">FilterAttachAtAltitude</a>. 

To detach a minifilter instance from a volume, call <a href="/windows/desktop/api/fltuser/nf-fltuser-filterdetach">FilterDetach</a>.

## -see-also

<a href="/windows/desktop/api/fltuser/nf-fltuser-filterattachataltitude">FilterAttachAtAltitude</a>



<a href="/windows/desktop/api/fltuser/nf-fltuser-filterdetach">FilterDetach</a>



<a href="/windows-hardware/drivers/ddi/content/fltkernel/nf-fltkernel-fltattachvolume">FltAttachVolume</a>