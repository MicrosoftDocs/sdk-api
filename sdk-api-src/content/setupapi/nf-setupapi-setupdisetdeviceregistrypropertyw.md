---
UID: NF:setupapi.SetupDiSetDeviceRegistryPropertyW
title: SetupDiSetDeviceRegistryPropertyW function
author: windows-sdk-content
description: The SetupDiSetDeviceRegistryProperty function sets a Plug and Play device property for a device.
old-location: devinst\setupdisetdeviceregistryproperty.htm
old-project: devinst
ms.assetid: 2686f416-3eb5-4e6b-87c8-ab10608ab406
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: SetupDiSetDeviceRegistryProperty, SetupDiSetDeviceRegistryProperty function [Device and Driver Installation], SetupDiSetDeviceRegistryPropertyA, SetupDiSetDeviceRegistryPropertyW, devinst.setupdisetdeviceregistryproperty, di-rtns_c3fa27e1-fbc6-4f82-ab1b-cbf3581c54e4.xml, setupapi/SetupDiSetDeviceRegistryProperty
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: setupapi.h
req.include-header: Setupapi.h
req.redist: 
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
tech.root: 
req.typenames: TSSD_ConnectionPoint, *PTSSD_ConnectionPoint
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - Setupapi.lib
 - Setupapi.dll
api_name:
 - SetupDiSetDeviceRegistryProperty
product: Windows
targetos: Windows
req.lib: Setupapi.lib
req.dll: 
req.irql: 
req.product: ADAM
---

# SetupDiSetDeviceRegistryPropertyW function


## -description


The <b>SetupDiSetDeviceRegistryProperty</b> function sets a Plug and Play device property for a device.


## -parameters




### -param DeviceInfoSet [in]

A handle to the <a href="devinst.device_information_sets">device information set</a> that contains a device information element that represents the device for which to set a Plug and Play device property.


### -param DeviceInfoData [in, out]

A pointer to an <a href="https://msdn.microsoft.com/9ad0ef4f-4a67-4f16-8bb1-2242dad0d041">SP_DEVINFO_DATA</a> structure that specifies the device information element in <i>DeviceInfoSet</i>. If the <b>ClassGuid</b> property is set, <i>DeviceInfoData.</i><b>ClassGuid</b> is set upon return to the new class for the device.


### -param Property [in]

One of the following values, which identifies the property to be set. For descriptions of these values, see <a href="https://msdn.microsoft.com/d42269dc-57b5-4303-94d9-02f6ee16a96f">SetupDiGetDeviceRegistryProperty</a>. 

<div class="alert"><b>Note</b>  <b>SPDRP_HARDWAREID</b> or <b>SPDRP_COMPATIBLEIDS</b> can only be used when <i>DeviceInfoData</i> represents a root-enumerated device. For other devices, the bus driver reports hardware and compatible IDs when enumerating a child device after receiving <a href="https://msdn.microsoft.com/3135cb30-a696-4201-8dfc-cdc1a29fe52b">IRP_MN_QUERY_ID</a>.</div>
<div> </div>
The following values are reserved for use by the operating system and cannot be used in the <i>Property</i> parameter:


### -param PropertyBuffer [in, optional]

A pointer to a buffer that contains the new data for the property. If the property is being cleared, then this pointer should be <b>NULL</b> and <i>PropertyBufferSize</i> must be zero.


### -param PropertyBufferSize [in]

The size, in bytes, of <i>PropertyBuffer</i>. If <i>PropertyBuffer</i> is <b>NULL</b>, then this field must be zero.


## -returns



The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved with a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>.




## -remarks



The caller of this function must be a member of the Administrators group.

The class name property cannot be set because it is based on the corresponding class GUID and is automatically updated when that property is changed. When the ClassGUID property changes, <b>SetupDiSetDeviceRegistryProperty</b> automatically cleans up any software keys associated with the device.




## -see-also




<a href="https://msdn.microsoft.com/79a600af-15c1-4afc-a2cd-568b97d979dc">SetupDiGetClassRegistryProperty</a>



<a href="https://msdn.microsoft.com/d42269dc-57b5-4303-94d9-02f6ee16a96f">SetupDiGetDeviceRegistryProperty</a>



<a href="https://msdn.microsoft.com/78457461-11ef-44ec-aa60-1adf4a48db8c">SetupDiSetClassRegistryProperty</a>
 

 

