---
UID: NF:setupapi.SetupDiUnremoveDevice
title: SetupDiUnremoveDevice function
author: windows-sdk-content
description: The SetupDiUnremoveDevice function is the default handler for the DIF_UNREMOVE installation request.
old-location: devinst\setupdiunremovedevice.htm
tech.root: devinst
ms.assetid: 1bffe874-d4ba-4efa-ab71-098a3c96092f
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: SetupDiUnremoveDevice, SetupDiUnremoveDevice function [Device and Driver Installation], devinst.setupdiunremovedevice, di-rtns_8c97341a-c852-47be-ad6e-c551f82deb6d.xml, setupapi/SetupDiUnremoveDevice
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: setupapi.h
req.include-header: Setupapi.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Microsoft Windows 2000 and later versions of Windows.
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
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Setupapi.dll
api_name:
 - SetupDiUnremoveDevice
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetupDiUnremoveDevice function


## -description


The <b>SetupDiUnremoveDevice</b> function is the default handler for the <a href="https://msdn.microsoft.com/01e39f77-3ee8-44c4-ba1a-19d4356b26ce">DIF_UNREMOVE</a> installation request. 


## -parameters




### -param DeviceInfoSet [in]

A handle to a <a href="devinst.device_information_sets">device information set</a> for the local system that contains a device information element that represents a device to restore and to restart.


### -param DeviceInfoData [in, out]

A pointer to an <a href="https://msdn.microsoft.com/9ad0ef4f-4a67-4f16-8bb1-2242dad0d041">SP_DEVINFO_DATA</a> structure that specifies the device information element in <i>DeviceInfoSet</i>. This is an IN-OUT parameter because <i>DeviceInfoData.</i><b>DevInst</b> might be updated with a new handle value on return. 


## -returns



The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved by a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>.




## -remarks



<b>SetupDiUnremoveDevice</b> restores a device to a hardware profile. This function starts the device, if possible, or it sets a flag in the device install parameters that eventually causes the user to be prompted to shut down the system.

<div class="alert"><b>Note</b>  Only a class installer should call <b>SetupDiUnremoveDevice</b> and only in those situations where the class installer must perform device unremove operations after <b>SetupDiUnremoveDevice</b> completes the default device unremove operation. In such situations, the class installer must directly call <b>SetupDiUnremoveDevice</b> when the installer processes a DIF_UNREMOVE request. For more information about calling the default handler, see <a href="devinst.calling_the_default_dif_code_handlers">Calling Default DIF Code Handlers</a>.</div>
<div> </div>
The device being restored must have class install parameters for <a href="https://msdn.microsoft.com/01e39f77-3ee8-44c4-ba1a-19d4356b26ce">DIF_UNREMOVE</a> or the function fails and <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a> returns ERROR_NO_CLASSINSTALL_PARAMS.

The <i>DeviceInfoSet</i> must only contain elements on the local computer.

The caller of <b>SetupDiUnremoveDevice</b> must be a member of the Administrators group.




## -see-also




<a href="https://msdn.microsoft.com/01e39f77-3ee8-44c4-ba1a-19d4356b26ce">DIF_UNREMOVE</a>



<a href="https://msdn.microsoft.com/9ad0ef4f-4a67-4f16-8bb1-2242dad0d041">SP_DEVINFO_DATA</a>



<a href="https://msdn.microsoft.com/1070f6cc-e5de-4f4e-8325-b412751e9fb3">SetupDiRemoveDevice</a>
 

 

