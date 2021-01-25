---
UID: NF:fltuser.FilterInstanceCreate
title: FilterInstanceCreate function (fltuser.h)
description: The FilterInstanceCreate function creates a handle that can be used to communicate with the given minifilter instance.
helpviewer_keywords: ["FilterInstanceCreate","FilterInstanceCreate function [Installable File System Drivers]","FltWin32ApiRef_eccac8f5-bc38-49ba-b2d8-cf505bec3641.xml","fltuser/FilterInstanceCreate","ifsk.filterinstancecreate"]
old-location: ifsk\filterinstancecreate.htm
tech.root: ifsk
ms.assetid: eb29fefc-285a-4a77-b1f6-1d42d029b7b7
ms.date: 12/05/2018
ms.keywords: FilterInstanceCreate, FilterInstanceCreate function [Installable File System Drivers], FltWin32ApiRef_eccac8f5-bc38-49ba-b2d8-cf505bec3641.xml, fltuser/FilterInstanceCreate, ifsk.filterinstancecreate
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
 - FilterInstanceCreate
 - fltuser/FilterInstanceCreate
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
 - FilterInstanceCreate
---

# FilterInstanceCreate function


## -description

The <b>FilterInstanceCreate</b> function creates a handle that can be used to communicate with the given minifilter instance.

## -parameters

### -param lpFilterName [in]

Pointer to a null-terminated wide-character string containing the name of the minifilter that owns the instance.

### -param lpVolumeName [in]

Pointer to a null-terminated wide-character string containing the name of the volume that the instance is attached to. 

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

### -param lpInstanceName [in, optional]

Pointer to a null-terminated wide-character string containing the instance name for the instance. This parameter is optional and can be <b>NULL</b>. If it is <b>NULL</b>, the first instance found for this minifilter on this volume is returned.

### -param hInstance [out]

Pointer to a caller-allocated variable that receives an opaque handle for the minifilter instance if the call to <b>FilterInstanceCreate</b> succeeds; otherwise, it receives INVALID_HANDLE_VALUE.

## -returns

<b>FilterInstanceCreate</b> returns S_OK if successful. Otherwise, it returns an error value.

## -remarks

A user-mode application calls <b>FilterInstanceCreate</b> to create a handle that can be used to communicate with a kernel-mode minifilter instance. The returned instance handle can be passed as a parameter to functions such as <a href="/windows/desktop/api/fltuser/nf-fltuser-filterinstancegetinformation">FilterInstanceGetInformation</a>. 

To close an instance handle returned by <b>FilterInstanceCreate</b>, call <a href="/windows/desktop/api/fltuser/nf-fltuser-filterinstanceclose">FilterInstanceClose</a>.

## -see-also

<a href="/windows/desktop/api/fltuser/nf-fltuser-filterinstanceclose">FilterInstanceClose</a>



<a href="/windows/desktop/api/fltuser/nf-fltuser-filterinstancegetinformation">FilterInstanceGetInformation</a>