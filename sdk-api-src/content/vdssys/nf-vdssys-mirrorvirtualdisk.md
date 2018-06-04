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

# MirrorVirtualDisk function


## -description


Initiates a mirror operation for a virtual disk.  Once the mirroring operation is initiated 
    it will not complete until either <a href="https://msdn.microsoft.com/b28162dc-0da8-41c6-9901-29381d2d72c4">CancelIo</a> or 
    <a href="https://msdn.microsoft.com/a2ce13b8-7da6-4848-848d-901d9667c2e3">CancelIoEx</a> is called to cancel all I/O on the 
    <i>VirtualDiskHandle</i>, leaving the original file as the current  or 
    <a href="https://msdn.microsoft.com/bf70ee43-9fba-4856-a1bc-85eec61f5763">BreakMirrorVirtualDisk</a> is called to stop using 
    the original file and only use the mirror. 
    <a href="https://msdn.microsoft.com/392a5258-306d-4c06-a632-85e6fc65ddc9">GetVirtualDiskOperationProgress</a> can be 
    used to determine if the disks are fully mirrored and writes go to both virtual disks.


## -parameters




### -param VirtualDiskHandle [in]

A handle to the open virtual disk. For information on how to open a virtual disk, see the 
      <a href="https://msdn.microsoft.com/08e2a82d-9110-42b1-be09-dc5150da42f6">OpenVirtualDisk</a> function.


### -param Flags [in]

A valid combination of values from the 
      <a href="https://msdn.microsoft.com/14051691-eacb-40b8-a8ae-822bc054d0a1">MIRROR_VIRTUAL_DISK_FLAG</a> enumeration.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MIRROR_VIRTUAL_DISK_FLAG_NONE"></a><a id="mirror_virtual_disk_flag_none"></a><dl>
<dt><b>MIRROR_VIRTUAL_DISK_FLAG_NONE</b></dt>
<dt>0x00000000</dt>
</dl>
</td>
<td width="60%">
The mirror virtual disk file does not exist, and needs to be created.

</td>
</tr>
<tr>
<td width="40%"><a id="MIRROR_VIRTUAL_DISK_FLAG_EXISTING_FILE"></a><a id="mirror_virtual_disk_flag_existing_file"></a><dl>
<dt><b>MIRROR_VIRTUAL_DISK_FLAG_EXISTING_FILE</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Create the mirror using an existing file.

</td>
</tr>
</table>
 


### -param Parameters [in]

Address of a 
      <a href="https://msdn.microsoft.com/bcde890e-24d5-41ac-8e5a-ba0d99e395e1">MIRROR_VIRTUAL_DISK_PARAMETERS</a> structure 
      containing mirror parameter data.


### -param Overlapped [in]

Address of an 
     <a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a>structure. This parameter is required.


## -returns



Status of the request.

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is an error code. For more information, see 
       <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/14051691-eacb-40b8-a8ae-822bc054d0a1">MIRROR_VIRTUAL_DISK_FLAG</a>



<a href="https://msdn.microsoft.com/bcde890e-24d5-41ac-8e5a-ba0d99e395e1">MIRROR_VIRTUAL_DISK_PARAMETERS</a>



<a href="https://msdn.microsoft.com/79c3b3ad-4eaf-49ce-a8ee-b26faf6c2cba">VHD Functions</a>
 

 

