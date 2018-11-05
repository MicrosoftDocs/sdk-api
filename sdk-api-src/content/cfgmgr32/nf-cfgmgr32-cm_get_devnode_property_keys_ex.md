---
UID: NF:cfgmgr32.CM_Get_DevNode_Property_Keys_Ex
title: CM_Get_DevNode_Property_Keys_Ex function
author: windows-sdk-content
description: The CM_Get_DevNode_Property_Keys_Ex function retrieves an array of the device property keys that represent the device properties that are set for a device instance.
old-location: devinst\cm_get_devnode_property_keys_ex.htm
tech.root: devinst
ms.assetid: E73358D5-7C7E-4D66-A7E7-566BBDC75ED0
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: CM_Get_DevNode_Property_Keys_Ex, CM_Get_DevNode_Property_Keys_Ex function [Device and Driver Installation], cfgmgr32/CM_Get_DevNode_Property_Keys_Ex, devinst.cm_get_devnode_property_keys_ex
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Cfgmgr32.lib; OneCoreUAP.lib on Windows 10
req.dll: CfgMgr32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - CfgMgr32.dll
 - API-MS-Win-devices-config-l1-1-0.dll
 - API-MS-Win-devices-config-l1-1-1.dll
api_name:
 - CM_Get_DevNode_Property_Keys_Ex
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CM_Get_DevNode_Property_Keys_Ex function


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.  Please use <a href="https://msdn.microsoft.com/3476FAA7-32EA-43A9-B7CF-3938F08E0AD1">CM_Get_DevNode_Property_Keys</a> instead.]

The <b>CM_Get_DevNode_Property_Keys_Ex</b> function retrieves an array of the device property keys that represent the device properties that are set for a device instance.


## -parameters




### -param dnDevInst [in]

Device instance handle that is bound to the local machine.


### -param PropertyKeyArray [out, optional]

Pointer to a buffer that receives an array of <a href="https://msdn.microsoft.com/98986d43-84c0-44e6-83f9-08e872ea5e6d">DEVPROPKEY</a>-typed values, where each value is a device property key that represents a device property that is set for the device instance. The pointer is optional and can be NULL.


### -param PropertyKeyCount [in, out]

The size, in <a href="https://msdn.microsoft.com/98986d43-84c0-44e6-83f9-08e872ea5e6d">DEVPROPKEY</a>-typed units, of the <i>PropertyKeyArray</i> buffer. If <i>PropertyKeyArray</i> is set to NULL, <i>*PropertyKeyCount</i> must be set to zero. As output, If <i>PropertyKeyArray</i> is not large enough to hold all the property key data, <b>CM_Get_DevNode_Property_Keys_Ex</b> returns the count of the keys in <i>*PropertyKeyCount</i>.


### -param ulFlags [in]

Reserved. Must be set to zero.


### -param hMachine [in, optional]

Caller-supplied machine handle, obtained from a previous call to <a href="https://msdn.microsoft.com/4108a35f-0861-4142-a798-731287515910">CM_Connect_Machine</a>.

<div class="alert"><b>Note</b>  Using this function to access remote machines is not supported beginning with Windows 8 and Windows Server 2012, as this functionality has been removed.</div>
<div> </div>

## -returns



If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.




## -remarks



<b>CM_Get_DevNode_Property_Keys_Ex</b> is part of the <a href="devinst.unified_device_property_model__windows_vista_and_later_">Unified Device Property Model</a>.




## -see-also




<a href="https://msdn.microsoft.com/4108a35f-0861-4142-a798-731287515910">CM_Connect_Machine</a>



<a href="https://msdn.microsoft.com/d4decdab-e412-4719-ad65-74f34cf8df27">SetupDiGetDevicePropertyKeys</a>
 

 

