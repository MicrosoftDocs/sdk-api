---
UID: NF:cfgmgr32.CM_Delete_Device_Interface_Key_ExW
title: CM_Delete_Device_Interface_Key_ExW function
author: windows-sdk-content
description: The CM_Delete_Device_Interface_Key_ExW function deletes the registry subkey that is used by applications and drivers to store interface-specific information.
old-location: devinst\cm_delete_device_interface_key_exw.htm
old-project: devinst
ms.assetid: 56BC813F-A1C1-4E3D-BDC1-13A7D9888EA7
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CM_Delete_Device_Interface_Key_ExW, CM_Delete_Device_Interface_Key_ExW function [Device and Driver Installation], cfgmgr32/CM_Delete_Device_Interface_Key_ExW, devinst.cm_delete_device_interface_key_exw
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: cfgmgr32.h
req.include-header: Cfgmgr32.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Microsoft Windows 10 and later versions of Windows.
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
 - CM_Delete_Device_Interface_Key_ExW
product: Windows
targetos: Windows
req.lib: Cfgmgr32.lib
req.dll: 
req.irql: 
---

# CM_Delete_Device_Interface_Key_ExW function


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.  Please use <a href="https://msdn.microsoft.com/library/windows/hardware/hh780215">CM_Delete_Device_Interface_Key</a> instead.]

The <b>CM_Delete_Device_Interface_Key_ExW</b> function deletes the registry subkey that is used by applications and drivers to store interface-specific information.


## -parameters




### -param pszDeviceInterface [in]

Pointer to a string that identifies the device interface instance of the registry subkey to delete.


### -param ulFlags [in]

Reserved. Must be set to zero.


### -param hMachine [in, optional]

Caller-supplied machine handle, obtained from a previous call to <a href="https://msdn.microsoft.com/library/windows/hardware/ff537948">CM_Connect_Machine</a>.

<div class="alert"><b>Note</b>  Using this function to access remote machines is not supported beginning with Windows 8 and Windows Server 2012, as this functionality has been removed.</div>
<div> </div>

## -returns



If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff537948">CM_Connect_Machine</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/hh780223">CM_Open_Device_Interface_Key</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550986">SetupDiDeleteDeviceInterfaceRegKey</a>
 

 

