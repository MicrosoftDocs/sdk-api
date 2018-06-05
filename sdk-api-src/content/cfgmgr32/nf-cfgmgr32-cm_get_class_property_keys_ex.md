---
UID: NF:cfgmgr32.CM_Get_Class_Property_Keys_Ex
title: CM_Get_Class_Property_Keys_Ex function
author: windows-sdk-content
description: The CM_Get_Class_Property_Keys_Ex function retrieves an array of the device property keys that represent the device properties that are set for a device interface class or device setup class.
old-location: devinst\cm_get_class_property_keys_ex.htm
old-project: devinst
ms.assetid: 78F3E4EE-BF06-464B-A570-021F9545D9AB
ms.author: windowssdkdev
ms.date: 05/31/2018
ms.keywords: CM_Get_Class_Property_Keys_Ex, CM_Get_Class_Property_Keys_Ex function [Device and Driver Installation], cfgmgr32/CM_Get_Class_Property_Keys_Ex, devinst.cm_get_class_property_keys_ex
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
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	CfgMgr32.dll
-	API-MS-Win-devices-config-l1-1-0.dll
-	API-MS-Win-devices-config-l1-1-1.dll
api_name:
-	CM_Get_Class_Property_Keys_Ex
product: Windows
targetos: Windows
req.lib: Cfgmgr32.lib; OneCoreUAP.lib on Windows 10
req.dll: CfgMgr32.dll
req.irql: 
---

# CM_Get_Class_Property_Keys_Ex function


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.  Please use <a href="https://msdn.microsoft.com/library/windows/hardware/hh780217">CM_Get_Class_Property_Keys</a> instead.]

The <b>CM_Get_Class_Property_Keys_Ex</b> function retrieves an array of the device property keys that represent the device properties that are set for a <a href="https://msdn.microsoft.com/C989D2D3-E8DE-4D64-86EE-3D3B3906390D">device interface class</a> or <a href="https://msdn.microsoft.com/en-us/library/windows/hardware/ff552344">device setup class</a>.


## -parameters




### -param ClassGUID [in]

Pointer to the GUID that identifies the <a href="https://msdn.microsoft.com/C989D2D3-E8DE-4D64-86EE-3D3B3906390D">device interface class</a> or <a href="https://msdn.microsoft.com/en-us/library/windows/hardware/ff552344">device setup class</a> for which to retrieve the property keys for. For information about specifying the class type, see the <i>ulFlags</i> parameter.


### -param PropertyKeyArray [out, optional]

Pointer to a buffer that receives an array of <a href="https://msdn.microsoft.com/library/windows/hardware/dn315031">DEVPROPKEY</a>-typed values, where each value is a device property key that represents a device property that is set for the device class. The pointer is optional and can be NULL.


### -param PropertyKeyCount [in, out]

The size, in <a href="https://msdn.microsoft.com/library/windows/hardware/dn315031">DEVPROPKEY</a>-typed units, of the <i>PropertyKeyArray</i> buffer. If <i>PropertyKeyArray</i> is set to NULL, <i>*PropertyKeyCount</i> must be set to zero. As output, if <i>PropertyKeyArray</i> is not large enough to hold all the property key data, <b>CM_Get_Class_Property_Keys_Ex</b> returns the count of the keys, in <i>*PropertyKeyCount</i>.


### -param ulFlags [in]

Class property key flags:





#### CM_CLASS_PROPERTY_INSTALLER

<i>ClassGUID</i> specifies a device setup class. Do not combine with CM_CLASS_PROPERTY_INTERFACE.



#### CM_CLASS_PROPERTY_INTERFACE

<i>ClassGUID</i> specifies a device interface class. Do not combine with CM_CLASS_PROPERTY_INSTALLER.


### -param hMachine [in, optional]

Caller-supplied machine handle, obtained from a previous call to <a href="https://msdn.microsoft.com/library/windows/hardware/ff537948">CM_Connect_Machine</a>.

<div class="alert"><b>Note</b>  Using this function to access remote machines is not supported beginning with Windows 8 and Windows Server 2012, as this functionality has been removed.</div>
<div> </div>

## -returns



If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.




## -remarks



<b>CM_Get_Class_Property_Keys_Ex</b> is part of the <a href="devinst.unified_device_property_model__windows_vista_and_later_">Unified Device Property Model</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff537948">CM_Connect_Machine</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551091">SetupDiGetClassPropertyKeys</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551093">SetupDiGetClassPropertyKeysEx</a>
 

 

