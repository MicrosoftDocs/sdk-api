---
UID: NF:cfgmgr32.CM_Set_Class_Property_ExW
title: CM_Set_Class_Property_ExW function
author: windows-sdk-content
description: The CM_Set_Class_Property_ExW function sets a class property for a device setup class or a device interface class.
old-location: devinst\cm_set_class_property_exw.htm
tech.root: devinst
ms.assetid: A2232661-DA67-40BB-81B9-0BC7851A6E25
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: CM_Set_Class_Property_ExW, CM_Set_Class_Property_ExW function [Device and Driver Installation], cfgmgr32/CM_Set_Class_Property_ExW, devinst.cm_set_class_property_exw
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
req.lib: Cfgmgr32.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - Cfgmgr32.lib
 - Cfgmgr32.dll
api_name:
 - CM_Set_Class_Property_ExW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CM_Set_Class_Property_ExW function


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.  Please use <a href="https://msdn.microsoft.com/BC026F97-4F4B-472F-83C0-FB5114AE1B7A">CM_Set_Class_Property</a> instead.]

The <b>CM_Set_Class_Property_ExW</b> function sets a class property for a device setup class or a device interface class.


## -parameters




### -param ClassGUID [in]

Pointer to the GUID that identifies the <a href="https://msdn.microsoft.com/C989D2D3-E8DE-4D64-86EE-3D3B3906390D">device interface class</a> or <a href="https://msdn.microsoft.com/en-us/library/windows/hardware/ff552344">device setup class</a> for which to set a device property. For information about specifying the class type, see the <i>ulFlags</i> parameter.


### -param PropertyKey [in]

Pointer to a <a href="https://msdn.microsoft.com/98986d43-84c0-44e6-83f9-08e872ea5e6d">DEVPROPKEY</a> structure that represents the property key of the device class property to set.


### -param PropertyType [in]

A <a href="https://msdn.microsoft.com/e0fdcc28-be70-4ae1-bd6d-89e2177eae62">DEVPROPTYPE</a>-typed value that represents the property-data-type identifier for the device class property. To delete a property, set this to <b>DEVPROP_TYPE_EMPTY</b>.


### -param PropertyBuffer [in]

Pointer to a buffer that contains the property value of the device class property. If either the property or the data is to be deleted, this pointer must be set to NULL, and <i>PropertyBufferSize</i> must be set to zero.


### -param PropertyBufferSize [in]

The size, in bytes, of the <i>PropertyBuffer</i> buffer. If <i>PropertyBuffer</i> is set to NULL, <i>PropertyBufferSize</i> must be set to zero.


### -param ulFlags [in]

Class property flags:





#### CM_CLASS_PROPERTY_INSTALLER

<i>ClassGUID</i> specifies a device setup class. Do not combine with CM_CLASS_PROPERTY_INTERFACE.



#### CM_CLASS_PROPERTY_INTERFACE

<i>ClassGUID</i> specifies a device interface class. Do not combine with CM_CLASS_PROPERTY_INSTALLER.


### -param hMachine [in, optional]

Caller-supplied machine handle, obtained from a previous call to <a href="https://msdn.microsoft.com/4108a35f-0861-4142-a798-731287515910">CM_Connect_Machine</a>.

<div class="alert"><b>Note</b>  Using this function to access remote machines is not supported beginning with Windows 8 and Windows Server 2012, as this functionality has been removed.</div>
<div> </div>

## -returns



If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.




## -remarks



<b>CM_Set_Class_Property_ExW</b> is part of the <a href="devinst.unified_device_property_model__windows_vista_and_later_">Unified Device Property Model</a>.




## -see-also




<a href="https://msdn.microsoft.com/4108a35f-0861-4142-a798-731287515910">CM_Connect_Machine</a>



<a href="https://msdn.microsoft.com/12402336-9894-4d0d-b176-c6907e0cdcd4">SetupDiSetClassProperty</a>
 

 

