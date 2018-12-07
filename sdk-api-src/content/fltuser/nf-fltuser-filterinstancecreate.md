---
UID: NF:fltuser.FilterInstanceCreate
title: FilterInstanceCreate function
author: windows-sdk-content
description: The FilterInstanceCreate function creates a handle that can be used to communicate with the given minifilter instance.
old-location: ifsk\filterinstancecreate.htm
tech.root: ifsk
ms.assetid: eb29fefc-285a-4a77-b1f6-1d42d029b7b7
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: FilterInstanceCreate, FilterInstanceCreate function [Installable File System Drivers], FltWin32ApiRef_eccac8f5-bc38-49ba-b2d8-cf505bec3641.xml, fltuser/FilterInstanceCreate, ifsk.filterinstancecreate
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: FltLib.lib
req.dll: FltLib.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - FltLib.dll
api_name:
 - FilterInstanceCreate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FilterInstanceCreate function


## -description


The <b>FilterInstanceCreate</b> function creates a handle that can be used to communicate with the given minifilter instance. 


## -parameters




### -param lpFilterName [in]

Pointer to a null-terminated wide-character string containing the name of the minifilter that owns the instance. 


### -param lpVolumeName [in]

Pointer to a null-terminated wide-character string containing the name of the volume that the instance is attached to. 

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

### -param lpInstanceName [in, optional]

Pointer to a null-terminated wide-character string containing the instance name for the instance. This parameter is optional and can be <b>NULL</b>. If it is <b>NULL</b>, the first instance found for this minifilter on this volume is returned. 


### -param hInstance [out]

Pointer to a caller-allocated variable that receives an opaque handle for the minifilter instance if the call to <b>FilterInstanceCreate</b> succeeds; otherwise, it receives INVALID_HANDLE_VALUE. 


## -returns



<b>FilterInstanceCreate</b> returns S_OK if successful. Otherwise, it returns an error value. 




## -remarks



A user-mode application calls <b>FilterInstanceCreate</b> to create a handle that can be used to communicate with a kernel-mode minifilter instance. The returned instance handle can be passed as a parameter to functions such as <a href="https://msdn.microsoft.com/222f5f68-6a1c-420e-a56f-de53b23f6ce6">FilterInstanceGetInformation</a>. 

To close an instance handle returned by <b>FilterInstanceCreate</b>, call <a href="https://msdn.microsoft.com/a0605b02-a5eb-4e7f-9659-0f0f538ea153">FilterInstanceClose</a>. 




## -see-also




<a href="https://msdn.microsoft.com/a0605b02-a5eb-4e7f-9659-0f0f538ea153">FilterInstanceClose</a>



<a href="https://msdn.microsoft.com/222f5f68-6a1c-420e-a56f-de53b23f6ce6">FilterInstanceGetInformation</a>
 

 

