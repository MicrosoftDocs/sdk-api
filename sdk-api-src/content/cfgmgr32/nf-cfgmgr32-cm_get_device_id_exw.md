---
UID: NF:cfgmgr32.CM_Get_Device_ID_ExW
title: CM_Get_Device_ID_ExW function
author: windows-sdk-content
description: The CM_Get_Device_ID_Ex function retrieves the device instance ID for a specified device instance on a local or a remote machine.
old-location: devinst\cm_get_device_id_ex.htm
old-project: devinst
ms.assetid: 757b8185-c5f5-4623-a410-63fd2f74e34f
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: CM_Get_Device_ID_Ex, CM_Get_Device_ID_Ex function [Device and Driver Installation], CM_Get_Device_ID_ExW, cfgmgr32/CM_Get_Device_ID_Ex, cfgmgr32/CM_Get_Device_ID_ExW, cfgmgrfn_e4ec7f8a-75aa-4c49-a2fe-a912685d5e98.xml, devinst.cm_get_device_id_ex
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: cfgmgr32.h
req.include-header: Cfgmgr32.h
req.redist: 
req.target-type: Desktop
req.target-min-winverclnt: Available in Microsoft Windows 2000 and later versions of Windows.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CM_Get_Device_ID_ExW (Unicode)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: CM_NOTIFY_ACTION, *PCM_NOTIFY_ACTION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - Cfgmgr32.lib
 - Cfgmgr32.dll
api_name:
 - CM_Get_Device_ID_Ex
 - CM_Get_Device_ID_ExW
product: Windows
targetos: Windows
req.lib: Cfgmgr32.lib
req.dll: 
req.irql: 
---

# CM_Get_Device_ID_ExW function


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.  Please use <a href="https://msdn.microsoft.com/924906ca-1119-428f-a42d-cb9a784af011">CM_Get_Device_ID</a> instead.]

The <b>CM_Get_Device_ID_Ex</b> function retrieves the <a href="https://msdn.microsoft.com/library/Ff541327(v=VS.85).aspx">device instance ID</a> for a specified <a href="https://msdn.microsoft.com/86688b5d-575d-42e1-9158-7ffba1aaf1d3">device instance</a> on a local or a remote machine.


## -parameters




### -param dnDevInst [in]

Caller-supplied device instance handle that is bound to the machine handle supplied by <i>hMachine</i>.
      
     


### -param Buffer [out]

Address of a buffer to receive a device instance ID string. The required buffer size can be obtained by calling <a href="https://msdn.microsoft.com/3b95f8e3-0059-4a2e-8c14-5938f5826faf">CM_Get_Device_ID_Size_Ex</a>, then incrementing the received value to allow room for the string's terminating <b>NULL</b>.


### -param BufferLen [in]

Caller-supplied length, in characters, of the buffer specified by <i>Buffer</i>.


### -param ulFlags [in]

Not used, must be zero.


### -param hMachine [in, optional]

Caller-supplied machine handle to which the caller-supplied device instance handle is bound.

<div class="alert"><b>Note</b>  Using this function to access remote machines is not supported beginning with Windows 8 and Windows Server 2012, as this functionality has been removed.</div>
<div> </div>

## -returns



If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.




## -remarks



The function appends a NULL terminator to the supplied <a href="https://msdn.microsoft.com/library/Ff541327(v=VS.85).aspx">device instance ID</a> string, unless the buffer is too small to hold the string. In this case, the function supplies as much of the identifier string as will fit into the buffer, and then returns CR_BUFFER_SMALL.

For information about device instance IDs, see <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/install/device-identification-strings">Device Identification Strings</a>.

For information about using device instance handles that are bound to a local or a remote machine, see <a href="https://msdn.microsoft.com/bcd46252-6f87-4d49-a24c-81789b0148d9">CM_Get_Child_Ex</a>.

 Functionality to access remote machines has been removed in Windows 8 and Windows Server 2012 and later operating systems thus you cannot access remote machines when running on these versions of Windows.




## -see-also




<a href="https://msdn.microsoft.com/bcd46252-6f87-4d49-a24c-81789b0148d9">CM_Get_Child_Ex</a>



<a href="https://msdn.microsoft.com/924906ca-1119-428f-a42d-cb9a784af011">CM_Get_Device_ID</a>
 

 

