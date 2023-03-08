---
UID: NF:fltuser.FilterDetach
title: FilterDetach function (fltuser.h)
description: The FilterDetach function detaches the given minifilter instance from the given volume.
helpviewer_keywords: ["FilterDetach","FilterDetach function [Installable File System Drivers]","FltWin32ApiRef_ee7eb095-922a-48c6-943a-0a54fb0789f1.xml","fltuser/FilterDetach","ifsk.filterdetach"]
old-location: ifsk\filterdetach.htm
tech.root: ifsk
ms.assetid: 798b1672-ea3a-418b-a52d-d57b15ed9426
ms.date: 12/05/2018
ms.keywords: FilterDetach, FilterDetach function [Installable File System Drivers], FltWin32ApiRef_ee7eb095-922a-48c6-943a-0a54fb0789f1.xml, fltuser/FilterDetach, ifsk.filterdetach
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
 - FilterDetach
 - fltuser/FilterDetach
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
 - FilterDetach
---

# FilterDetach function


## -description

The <b>FilterDetach</b> function detaches the given minifilter instance from the given volume.

## -parameters

### -param lpFilterName [in]

Pointer to a null-terminated wide-character string containing the name of the minifilter whose instance is to be detached from the stack. This parameter is required and cannot be <b>NULL</b>.

### -param lpVolumeName [in]

Pointer to a null-terminated wide-character string containing the name of the volume to which the instance is currently attached. 

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
This parameter is required and cannot be <b>NULL</b>.

### -param lpInstanceName [in, optional]

Pointer to a null-terminated wide-character string containing the instance name for the instance to be removed. This parameter is optional and can be <b>NULL</b>. If it is <b>NULL</b>, the highest matching instance is removed.

## -returns

<b>FilterDetach</b> returns S_OK if successful. Otherwise, it returns an error value.

## -remarks

<b>FilterDetach</b> is the Win32 equivalent of <a href="/windows-hardware/drivers/ddi/content/fltkernel/nf-fltkernel-fltdetachvolume">FltDetachVolume</a>. 

<b>FilterDetach</b> detaches a minifilter instance from a volume and tears down the instance. 

To attach a minifilter instance to a volume, call <a href="/windows/desktop/api/fltuser/nf-fltuser-filterattach">FilterAttach</a> or <a href="/windows/desktop/api/fltuser/nf-fltuser-filterattachataltitude">FilterAttachAtAltitude</a>.

## -see-also

<a href="/windows/desktop/api/fltuser/nf-fltuser-filterattach">FilterAttach</a>



<a href="/windows/desktop/api/fltuser/nf-fltuser-filterattachataltitude">FilterAttachAtAltitude</a>



<a href="/windows-hardware/drivers/ddi/content/fltkernel/nf-fltkernel-fltdetachvolume">FltDetachVolume</a>