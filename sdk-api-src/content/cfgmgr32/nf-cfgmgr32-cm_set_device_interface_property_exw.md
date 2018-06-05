---
UID: NF:cfgmgr32.CM_Set_Device_Interface_Property_ExW
title: CM_Set_Device_Interface_Property_ExW function
author: windows-sdk-content
description: The CM_Set_Device_Interface_Property_ExW function sets a device property of a device interface.
old-location: devinst\cm_set_device_interface_property_exw.htm
old-project: devinst
ms.assetid: E3873F92-B2A7-4DDF-8C14-23D6815EE21E
ms.author: windowssdkdev
ms.date: 05/31/2018
ms.keywords: CM_Set_Device_Interface_Property_ExW, CM_Set_Device_Interface_Property_ExW function [Device and Driver Installation], cfgmgr32/CM_Set_Device_Interface_Property_ExW, devinst.cm_set_device_interface_property_exw
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
-	LibDef
api_location:
-	Cfgmgr32.lib
-	Cfgmgr32.dll
api_name:
-	CM_Set_Device_Interface_Property_ExW
product: Windows
targetos: Windows
req.lib: Cfgmgr32.lib
req.dll: 
req.irql: 
---

# CM_Set_Device_Interface_Property_ExW function


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.  Please use <a href="https://msdn.microsoft.com/library/windows/hardware/hh780226">CM_Set_Device_Interface_Property</a> instead.]

The <b>CM_Set_Device_Interface_Property_ExW</b> function sets a device property of a device interface.


## -parameters




### -param pszDeviceInterface [in]

Pointer to a string that identifies the device interface instance for which to set a property for.


### -param PropertyKey [in]

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/dn315031">DEVPROPKEY</a> structure that represents the property key of the device interface property to set.


### -param PropertyType [in]

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff543546">DEVPROPTYPE</a>-typed value that represents the property-data-type identifier for the device interface property. To delete a property, this must be set to DEVPROP_TYPE_EMPTY.


### -param PropertyBuffer [in]

Pointer to a buffer that contains the property value of the device interface property. If either the property or the data is being deleted, this pointer must be set to NULL, and <i>PropertyBufferSize</i> must be set to zero.


### -param PropertyBufferSize [in]

The size, in bytes, of the <i>PropertyBuffer</i> buffer. If <i>PropertyBuffer</i> is set to NULL, <i>PropertyBufferSize</i> must be set to zero.


### -param ulFlags [in]

Reserved. Must be set to zero.


### -param hMachine [in, optional]

Caller-supplied machine handle, obtained from a previous call to <a href="https://msdn.microsoft.com/library/windows/hardware/ff537948">CM_Connect_Machine</a>.

<div class="alert"><b>Note</b>  Using this function to access remote machines is not supported beginning with Windows 8 and Windows Server 2012, as this functionality has been removed.</div>
<div> </div>

## -returns



If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.




## -remarks



<b>CM_Set_Device_Interface_Property_ExW</b> is part of the <a href="devinst.unified_device_property_model__windows_vista_and_later_">Unified Device Property Model</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff537948">CM_Connect_Machine</a>



<a href="https://msdn.microsoft.com/5c8da8a3-1c53-42c1-8adc-46743b63f731">SetupDiSetDeviceInterfaceProperty</a>
 

 

