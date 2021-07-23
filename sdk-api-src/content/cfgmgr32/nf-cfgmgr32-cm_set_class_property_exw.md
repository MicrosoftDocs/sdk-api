---
UID: NF:cfgmgr32.CM_Set_Class_Property_ExW
title: CM_Set_Class_Property_ExW function (cfgmgr32.h)
description: The CM_Set_Class_Property_ExW function sets a class property for a device setup class or a device interface class.
helpviewer_keywords: ["CM_Set_Class_Property_ExW","CM_Set_Class_Property_ExW function [Device and Driver Installation]","cfgmgr32/CM_Set_Class_Property_ExW","devinst.cm_set_class_property_exw"]
old-location: devinst\cm_set_class_property_exw.htm
tech.root: devinst
ms.assetid: A2232661-DA67-40BB-81B9-0BC7851A6E25
ms.date: 12/05/2018
ms.keywords: CM_Set_Class_Property_ExW, CM_Set_Class_Property_ExW function [Device and Driver Installation], cfgmgr32/CM_Set_Class_Property_ExW, devinst.cm_set_class_property_exw
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CM_Set_Class_Property_ExW
 - cfgmgr32/CM_Set_Class_Property_ExW
dev_langs:
 - c++
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
---

# CM_Set_Class_Property_ExW function


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.  Please use <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_set_class_propertyw">CM_Set_Class_Property</a> instead.]

The <b>CM_Set_Class_Property_ExW</b> function sets a class property for a device setup class or a device interface class.

## -parameters

### -param ClassGUID [in]

Pointer to the GUID that identifies the <a href="/windows-hardware/drivers/install/overview-of-device-interface-classes">device interface class</a> or <a href="/windows-hardware/drivers/install/overview-of-device-setup-classes">device setup class</a> for which to set a device property. For information about specifying the class type, see the <i>ulFlags</i> parameter.

### -param PropertyKey [in]

Pointer to a <a href="/windows-hardware/drivers/install/devpropkey">DEVPROPKEY</a> structure that represents the property key of the device class property to set.

### -param PropertyType [in]

A <a href="/windows-hardware/drivers/install/property-data-type-identifiers">DEVPROPTYPE</a>-typed value that represents the property-data-type identifier for the device class property. To delete a property, set this to <b>DEVPROP_TYPE_EMPTY</b>.

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

Caller-supplied machine handle, obtained from a previous call to <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_connect_machinew">CM_Connect_Machine</a>.

<div class="alert"><b>Note</b>  Using this function to access remote machines is not supported beginning with Windows 8 and Windows Server 2012, as this functionality has been removed.</div>
<div> </div>

## -returns

If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.

## -remarks

<b>CM_Set_Class_Property_ExW</b> is part of the <a href="/windows-hardware/drivers/install/unified-device-property-model--windows-vista-and-later-">Unified Device Property Model</a>.

## -see-also

<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_connect_machinew">CM_Connect_Machine</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdisetclasspropertyw">SetupDiSetClassProperty</a>