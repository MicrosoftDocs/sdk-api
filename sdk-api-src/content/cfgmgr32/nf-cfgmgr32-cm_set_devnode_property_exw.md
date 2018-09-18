---
UID: NF:cfgmgr32.CM_Set_DevNode_Property_ExW
title: CM_Set_DevNode_Property_ExW function
author: windows-sdk-content
description: The CM_Set_DevNode_Property_ExW function sets a device instance property.
old-location: devinst\cm_set_devnode_property_exw.htm
tech.root: devinst
ms.assetid: FB725245-DB20-4363-BEC0-D7C837BED78A
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: CM_Set_DevNode_Property_ExW, CM_Set_DevNode_Property_ExW function [Device and Driver Installation], cfgmgr32/CM_Set_DevNode_Property_ExW, devinst.cm_set_devnode_property_exw
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
 - CM_Set_DevNode_Property_ExW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CM_Set_DevNode_Property_ExW function


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.  Please use <a href="https://msdn.microsoft.com/D6511A3B-F324-4153-8EAE-8C970AAE4E9D">CM_Set_DevNode_Property</a> instead.]

The <b>CM_Set_DevNode_Property_ExW</b> function sets a device instance property.


## -parameters




### -param dnDevInst [in]

Device instance handle that is bound to the local machine.


### -param PropertyKey [in]

Pointer to a <a href="https://msdn.microsoft.com/98986d43-84c0-44e6-83f9-08e872ea5e6d">DEVPROPKEY</a> structure that represents the property key of the device instance property to set.


### -param PropertyType [in]

A <a href="https://msdn.microsoft.com/e0fdcc28-be70-4ae1-bd6d-89e2177eae62">DEVPROPTYPE</a>-typed value that represents the property-data-type identifier for the device instance property. To delete a property, this must be set to DEVPROP_TYPE_EMPTY.


### -param PropertyBuffer [in]

Pointer to a buffer that contains the property value of the device instance property. If either the property or the data is being deleted, this pointer must be set to NULL, and <i>PropertyBufferSize</i> must be set to zero.


### -param PropertyBufferSize [in]

The size, in bytes, of the <i>PropertyBuffer</i> buffer. If <i>PropertyBuffer</i> is set to NULL, <i>PropertyBufferSize</i> must be set to zero.


### -param ulFlags [in]

Reserved. Must be set to zero.


### -param hMachine [in, optional]

Caller-supplied machine handle, obtained from a previous call to <a href="https://msdn.microsoft.com/4108a35f-0861-4142-a798-731287515910">CM_Connect_Machine</a>.

<div class="alert"><b>Note</b>  Using this function to access remote machines is not supported beginning with Windows 8 and Windows Server 2012, as this functionality has been removed.</div>
<div> </div>

## -returns



If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.




## -remarks



<b>CM_Set_DevNode_Property_ExW</b> is part of the <a href="devinst.unified_device_property_model__windows_vista_and_later_">Unified Device Property Model</a>.




## -see-also




<a href="https://msdn.microsoft.com/4108a35f-0861-4142-a798-731287515910">CM_Connect_Machine</a>



<a href="https://msdn.microsoft.com/c03c51ba-3027-4be9-8869-6d7dbeac2428">SetupDiSetDeviceProperty</a>
 

 

