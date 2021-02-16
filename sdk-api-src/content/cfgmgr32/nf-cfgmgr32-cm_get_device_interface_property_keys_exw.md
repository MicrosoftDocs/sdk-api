---
UID: NF:cfgmgr32.CM_Get_Device_Interface_Property_Keys_ExW
title: CM_Get_Device_Interface_Property_Keys_ExW function (cfgmgr32.h)
description: The CM_Get_Device_Interface_Property_Keys_ExW function retrieves an array of device property keys that represent the device properties that are set for a device interface.
helpviewer_keywords: ["CM_Get_Device_Interface_Property_Keys_ExW","CM_Get_Device_Interface_Property_Keys_ExW function [Device and Driver Installation]","cfgmgr32/CM_Get_Device_Interface_Property_Keys_ExW","devinst.cm_get_device_interface_property_keys_exw"]
old-location: devinst\cm_get_device_interface_property_keys_exw.htm
tech.root: devinst
ms.assetid: 52EEF50F-4559-4C22-BE33-1F87E469BB47
ms.date: 12/05/2018
ms.keywords: CM_Get_Device_Interface_Property_Keys_ExW, CM_Get_Device_Interface_Property_Keys_ExW function [Device and Driver Installation], cfgmgr32/CM_Get_Device_Interface_Property_Keys_ExW, devinst.cm_get_device_interface_property_keys_exw
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
 - CM_Get_Device_Interface_Property_Keys_ExW
 - cfgmgr32/CM_Get_Device_Interface_Property_Keys_ExW
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
 - CM_Get_Device_Interface_Property_Keys_ExW
---

# CM_Get_Device_Interface_Property_Keys_ExW function


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.  Please use <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_device_interface_property_keysw">CM_Get_Device_Interface_Property_Keys</a> instead.]

The <b>CM_Get_Device_Interface_Property_Keys_ExW</b> function retrieves an array of device property keys that represent the device properties that are set for a device interface.

## -parameters

### -param pszDeviceInterface [in]

Pointer to a string that identifies the device interface instance to retrieve the property keys from.

### -param PropertyKeyArray [out, optional]

Pointer to a buffer that receives an array of <a href="/windows-hardware/drivers/install/devpropkey">DEVPROPKEY</a>-typed values, where each value is a device property key that represents a device property that is set for the device interface. The pointer is optional and can be NULL

### -param PropertyKeyCount [in, out]

The size, in <a href="/windows-hardware/drivers/install/devpropkey">DEVPROPKEY</a>-typed units, of the <i>PropertyKeyArray</i> buffer. If <i>PropertyKeyArray</i> is set to NULL, <i>*PropertyKeyCount</i> must be set to zero.  As output, if <i>PropertyKeyArray</i> is not large enough to hold all the property key data, <b>CM_Get_Device_Interface_Property_Keys_ExW</b> returns the count of the keys, in <i>*PropertyKeyCount</i>.

### -param ulFlags [in]

Reserved. Must be set to zero.

### -param hMachine [in, optional]

Caller-supplied machine handle, obtained from a previous call to <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_connect_machinew">CM_Connect_Machine</a>.

<div class="alert"><b>Note</b>  Using this function to access remote machines is not supported beginning with Windows 8 and Windows Server 2012, as this functionality has been removed.</div>
<div> </div>

## -returns

If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.

## -remarks

<b>CM_Get_Device_Interface_Property_Keys_ExW</b> is part of the <a href="/windows-hardware/drivers/install/unified-device-property-model--windows-vista-and-later-">Unified Device Property Model</a>.

## -see-also

<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_connect_machinew">CM_Connect_Machine</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetdeviceinterfacepropertykeys">SetupDiGetDeviceInterfacePropertyKeys</a>