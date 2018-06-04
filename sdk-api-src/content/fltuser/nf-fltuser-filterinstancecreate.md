---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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



A user-mode application calls <b>FilterInstanceCreate</b> to create a handle that can be used to communicate with a kernel-mode minifilter instance. The returned instance handle can be passed as a parameter to functions such as <a href="https://msdn.microsoft.com/library/windows/hardware/ff541499">FilterInstanceGetInformation</a>. 

To close an instance handle returned by <b>FilterInstanceCreate</b>, call <a href="https://msdn.microsoft.com/library/windows/hardware/ff540524">FilterInstanceClose</a>. 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff540524">FilterInstanceClose</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff541499">FilterInstanceGetInformation</a>
 

 

