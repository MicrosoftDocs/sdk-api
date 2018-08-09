---
UID: NF:fltuser.FilterDetach
title: FilterDetach function
author: windows-sdk-content
description: The FilterDetach function detaches the given minifilter instance from the given volume.
old-location: ifsk\filterdetach.htm
old-project: ifsk
ms.assetid: 798b1672-ea3a-418b-a52d-d57b15ed9426
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: FilterDetach, FilterDetach function [Installable File System Drivers], FltWin32ApiRef_ee7eb095-922a-48c6-943a-0a54fb0789f1.xml, fltuser/FilterDetach, ifsk.filterdetach
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: FILTERED_DATA_SOURCES
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - FltLib.dll
api_name:
 - FilterDetach
product: Windows
targetos: Windows
req.lib: FltLib.lib
req.dll: FltLib.dll
req.irql: 
req.product: Internet Explorer 5
---

# FilterDetach function


## -description


The <b>FilterDetach</b> function detaches the given minifilter instance from the given volume. 


## -parameters




### -param lpFilterName [in]

Pointer to a null-terminated wide-character string containing the name of the minifilter whose instance is to be detached from the stack. This parameter is required and cannot be <b>NULL</b>. 


### -param lpVolumeName [in]

Pointer to a null-terminated wide-character string containing the name of the volume to which the instance is currently attached. 

The <i>lpVolumeName</i> input string can be any of the following. The trailing backslash (\) is optional. 

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



<b>FilterDetach</b> is the Win32 equivalent of <a href="https://msdn.microsoft.com/library/windows/hardware/ff542041">FltDetachVolume</a>. 

<b>FilterDetach</b> detaches a minifilter instance from a volume and tears down the instance. 

To attach a minifilter instance to a volume, call <a href="https://msdn.microsoft.com/library/windows/hardware/ff540442">FilterAttach</a> or <a href="https://msdn.microsoft.com/library/windows/hardware/ff540448">FilterAttachAtAltitude</a>. 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff540442">FilterAttach</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff540448">FilterAttachAtAltitude</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff542041">FltDetachVolume</a>
 

 

