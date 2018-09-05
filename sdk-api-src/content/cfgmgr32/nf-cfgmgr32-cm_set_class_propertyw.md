---
UID: NF:cfgmgr32.CM_Set_Class_PropertyW
title: CM_Set_Class_PropertyW function
author: windows-sdk-content
description: The CM_Set_Class_Property function sets a class property for a device setup class or a device interface class.
old-location: devinst\cm_set_class_property.htm
old-project: devinst
ms.assetid: BC026F97-4F4B-472F-83C0-FB5114AE1B7A
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: CM_Set_Class_Property, CM_Set_Class_Property function [Device and Driver Installation], CM_Set_Class_PropertyW, cfgmgr32/CM_Set_Class_Property, cfgmgr32/CM_Set_Class_PropertyW, devinst.cm_set_class_property
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: cfgmgr32.h
req.include-header: Cfgmgr32.h
req.redist: 
req.target-type: Universal
req.target-min-winverclnt: Available in Microsoft Windows Vista and later versions of Windows.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CM_Set_Class_PropertyW (Unicode)
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
 - DllExport
api_location:
 - Cfgmgr32.lib
 - Cfgmgr32.dll
 - API-Ms-Win-Devices-Config-L1-1-0.dll
 - API-Ms-Win-Devices-Config-L1-1-1.dll
 - CfgMgr32.dll
api_name:
 - CM_Set_Class_Property
 - CM_Set_Class_PropertyW
product: Windows
targetos: Windows
req.lib: Cfgmgr32.lib
req.dll: 
req.irql: 
---

# CM_Set_Class_PropertyW function


## -description


The <b>CM_Set_Class_Property</b> function sets a class property for a device setup class or a device interface class.


## -parameters




### -param ClassGUID [in]

Pointer to the GUID that identifies the <a href="https://msdn.microsoft.com/C989D2D3-E8DE-4D64-86EE-3D3B3906390D">device interface class</a> or <a href="https://msdn.microsoft.com/en-us/library/windows/hardware/ff552344">device setup class</a> for which to set a device property. For information about specifying the class type, see the <i>ulFlags</i> parameter.


### -param PropertyKey [in]

Pointer to a <a href="https://msdn.microsoft.com/98986d43-84c0-44e6-83f9-08e872ea5e6d">DEVPROPKEY</a> structure that represents the property key of the device class property to set.


### -param PropertyType [in]

A <a href="https://msdn.microsoft.com/e0fdcc28-be70-4ae1-bd6d-89e2177eae62">DEVPROPTYPE</a>-typed value that represents the property-data-type identifier for the device class property. To delete a property, set this to DEVPROP_TYPE_EMPTY.


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


## -returns



If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.




## -remarks



<b>CM_Set_Class_Property</b> is part of the <a href="devinst.unified_device_property_model__windows_vista_and_later_">Unified Device Property Model</a>.




## -see-also




<a href="https://msdn.microsoft.com/12402336-9894-4d0d-b176-c6907e0cdcd4">SetupDiSetClassProperty</a>
 

 

