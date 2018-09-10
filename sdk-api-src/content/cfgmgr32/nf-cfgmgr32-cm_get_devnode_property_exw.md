---
UID: NF:cfgmgr32.CM_Get_DevNode_Property_ExW
title: CM_Get_DevNode_Property_ExW function
author: windows-sdk-content
description: The CM_Get_DevNode_Property_ExW function retrieves a device instance property.
old-location: devinst\cm_get_devnode_property_exw.htm
tech.root: devinst
ms.assetid: 6766C495-0DAA-41E6-BB62-6FD21718FF8D
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: CM_Get_DevNode_Property_ExW, CM_Get_DevNode_Property_ExW function [Device and Driver Installation], cfgmgr32/CM_Get_DevNode_Property_ExW, devinst.cm_get_devnode_property_exw
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
 - CM_Get_DevNode_Property_ExW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CM_Get_DevNode_Property_ExW function


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.  Please use <a href="https://msdn.microsoft.com/A2EE0C78-13CB-4D9D-B68C-F527CCA2DF26">CM_Get_DevNode_Property</a> instead.]

The <b>CM_Get_DevNode_Property_ExW</b> function retrieves a device instance property.


## -parameters




### -param dnDevInst [in]

Device instance handle that is bound to the local machine.


### -param PropertyKey [in]

Pointer to a <a href="https://msdn.microsoft.com/98986d43-84c0-44e6-83f9-08e872ea5e6d">DEVPROPKEY</a> structure that represents the device property key of the requested device instance property.


### -param PropertyType [out]

Pointer to a <a href="https://msdn.microsoft.com/e0fdcc28-be70-4ae1-bd6d-89e2177eae62">DEVPROPTYPE</a>-typed variable that receives the property-data-type identifier of the requested device instance property, where the property-data-type identifier is the bitwise OR between a base-data-type identifier and, if the base-data type is modified, a property-data-type modifier.


### -param PropertyBuffer [out]

Pointer to a buffer that receives the requested device instance property. <b>CM_Get_DevNode_Property_ExW</b> retrieves the requested property only if the buffer is large enough to hold all the property value data. The pointer can be NULL.


### -param PropertyBufferSize [in, out]

The size, in bytes, of the <i>PropertyBuffer</i> buffer. If <i>PropertyBuffer</i> is set to NULL, <i>*PropertyBufferSize</i> must be set to zero. As output, if the buffer is not large enough to hold all the property value data, <b>CM_Get_DevNode_Property_ExW</b> returns the size of the data, in bytes, in <i>*PropertyBufferSize</i>.


### -param ulFlags [in]

Reserved. Must be set to zero.


### -param hMachine [in, optional]

Caller-supplied machine handle, obtained from a previous call to <a href="https://msdn.microsoft.com/4108a35f-0861-4142-a798-731287515910">CM_Connect_Machine</a>.

<div class="alert"><b>Note</b>  Using this function to access remote machines is not supported beginning with Windows 8 and Windows Server 2012, as this functionality has been removed.</div>
<div> </div>

## -returns



If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.




## -remarks



<b>CM_Get_DevNode_Property_ExW</b> is part of the <a href="devinst.unified_device_property_model__windows_vista_and_later_">Unified Device Property Model</a>.




## -see-also




<a href="https://msdn.microsoft.com/4108a35f-0861-4142-a798-731287515910">CM_Connect_Machine</a>



<a href="https://msdn.microsoft.com/eac31612-e80b-44ad-b4d4-a4aa014e833f">SetupDiGetDeviceProperty</a>
 

 

