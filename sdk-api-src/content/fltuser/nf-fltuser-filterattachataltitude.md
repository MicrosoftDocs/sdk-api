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

# FilterAttachAtAltitude function


## -description


The <b>FilterAttachAtAltitude</b> function is a debugging support function that attaches a new minifilter instance to a volume at a specified altitude, overriding any settings in the minifilter's setup information (INF) file. 


## -parameters




### -param lpFilterName [in]

Pointer to a null-terminated wide-character string containing the name of the minifilter for which an instance is to be created. This parameter is required and cannot be <b>NULL</b>. 


### -param lpVolumeName [in]

Pointer to a null-terminated wide-character string containing the name of the volume to which the newly created instance is to be attached. 

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


### -param lpAltitude [in]

Pointer to a null-terminated wide-character string that contains a numeric value specifying the target position that the minifilter instance should occupy in the stack for the volume. The higher the number, the higher the relative position in the stack. An altitude string consists of one or more digits in the range from 0 through 9, and it can include a single decimal point. The decimal point is optional. For example, "100.123456" is a valid altitude string. This parameter is required and cannot be <b>NULL</b>. 


### -param lpInstanceName [in, optional]

Pointer to a null-terminated wide-character string containing the instance name for the new instance. This parameter is optional and can be <b>NULL</b>. If this parameter is <b>NULL</b>, the new instance receives the minifilter's default instance name as described in the Remarks section for <a href="https://msdn.microsoft.com/library/windows/hardware/ff541772">FltAttachVolume</a>. 


### -param dwCreatedInstanceNameLength [in, optional]

Length, in bytes, of the buffer that <i>lpCreatedInstanceName </i>points to. This parameter is optional and can be zero. 


### -param lpCreatedInstanceName [out, optional]

Pointer to a caller-allocated variable that receives the instance name for the new instance if the instance is successfully attached to the volume. This parameter is optional and can be <b>NULL</b>. If it is not <b>NULL</b>, the buffer must be large enough to hold INSTANCE_NAME_MAX_CHARS characters plus a NULL terminator. 


## -returns



<b>FilterAttachAtAltitude</b> returns S_OK if successful. Otherwise, it returns an error value such as one of the following. 

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
</table>
 




## -remarks



An application should only use <b>FilterAttachAtAltitude</b> for debugging. It should not call this function in a retail version of the application. 

<b>FilterAttachAtAltitude</b> is the Win32 equivalent of <a href="https://msdn.microsoft.com/library/windows/hardware/ff541775">FltAttachVolumeAtAltitude</a>. 

The term "altitude" refers to the position that an instance occupies (or should occupy) in the minifilter instance stack for a volume. The higher the altitude, the farther the instance is from the base file system in the stack. Only one instance can be attached at a given altitude on a given volume. 

Altitude is specified by an <i>altitude string</i>, which is a wide-character array containing one or more decimal digits in the range from 0 through 9, and it can include a single decimal point. The decimal point is optional. For example, "100.123456" and "03333" are valid altitude strings. 

The string "03333" represents a higher altitude than "100.123456". (Leading and trailing zeros are ignored.) In other words, an instance whose altitude is "03333" is farther from the base file system than an instance whose altitude is "100.123456". However, this comparison is only meaningful if both instances are attached to the same volume. 

The instance name returned in <i>lpCreatedInstanceName</i> is unique across the system. 

To detach a minifilter instance from a volume, call <a href="https://msdn.microsoft.com/library/windows/hardware/ff540475">FilterDetach</a>. 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff540442">FilterAttach</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff540475">FilterDetach</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff541775">FltAttachVolumeAtAltitude</a>
 

 

