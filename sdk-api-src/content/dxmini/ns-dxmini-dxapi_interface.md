---
UID: NS:dxmini._DXAPI_INTERFACE
title: DXAPI_INTERFACE (dxmini.h)
author: windows-sdk-content
description: The DXAPI_INTERFACE structure contains the interface callback functions that a video miniport driver implements to support Kernel-Mode Video Transport.
old-location: display\dxapi_interface.htm
tech.root: display
ms.assetid: 137473ea-4785-4118-86af-a859f69f425f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PDXAPI_INTERFACE, DXAPI_INTERFACE, DXAPI_INTERFACE structure [Display Devices], PDXAPI_INTERFACE, PDXAPI_INTERFACE structure pointer [Display Devices], ddstrcts_99854747-7e4c-4a5a-9252-13f56abdffbc.xml, display.dxapi_interface, dxmini/DXAPI_INTERFACE, dxmini/PDXAPI_INTERFACE"
ms.topic: struct
req.header: dxmini.h
req.include-header: Dxmini.h
req.target-type: Windows
req.target-min-winverclnt: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxmini.h
api_name:
 - DXAPI_INTERFACE
product: Windows
targetos: Windows
req.typenames: DXAPI_INTERFACE, *PDXAPI_INTERFACE
req.redist: 
ms.custom: 19H1
---

# DXAPI_INTERFACE structure


## -description


The DXAPI_INTERFACE structure contains the interface callback functions that a <a href="https://msdn.microsoft.com/3a540bfe-f340-4f12-acee-323b97683074">video miniport driver</a> implements to support <a href="https://msdn.microsoft.com/3acaabc7-8d9f-441b-9170-2e5a4e0ce114">Kernel-Mode Video Transport</a>.


## -struct-fields




### -field Size

Specifies the size in bytes of this DXAPI_INTERFACE structure.


### -field Version

Specifies the version of the video miniport driver's <a href="https://msdn.microsoft.com/cfe77d14-32d2-44b7-8121-20ae7e4fe79e">DxApi interface</a>. This value is DXAPI_HALVERSION defined in <i>dxmini.h</i>.


### -field Context

Points to the device extension of the device. 


### -field InterfaceReference

Unused by the driver. 


### -field InterfaceDereference

Unused by the driver. 


### -field DxGetIrqInfo

Points to the driver-supplied <a href="https://msdn.microsoft.com/bc7463ab-1cb1-4ce5-a929-1513507a16ff">DxGetIRQInfo</a> miniport driver callback function.


### -field DxEnableIrq

Points to the driver-supplied <a href="https://msdn.microsoft.com/31762a21-e604-4c95-b46c-224b39ab5ac8">DxEnableIRQ</a> miniport driver callback function.


### -field DxSkipNextField

Points to the driver-supplied <a href="https://msdn.microsoft.com/da19c8dc-fef5-41e6-b032-2a0ae05a73da">DxSkipNextField</a> miniport driver callback function.


### -field DxBobNextField

Points to the driver-supplied <a href="https://msdn.microsoft.com/5daafc0c-2a6d-45e2-8403-d54cb383b3b7">DxBobNextField</a> miniport driver callback function.


### -field DxSetState

Points to the driver-supplied <a href="https://msdn.microsoft.com/f2d7f248-017e-4375-b0a0-49de65192511">DxSetState</a> miniport driver callback function.


### -field DxLock

Points to the driver-supplied <a href="https://msdn.microsoft.com/1eeeb68b-9098-4030-924a-634e79c3e682">DxLock</a> miniport driver callback function.


### -field DxFlipOverlay

Points to the driver-supplied <a href="https://msdn.microsoft.com/7674f853-e5ea-44c7-b5ed-5fd90bfa1bcb">DxFlipOverlay</a> miniport driver callback function.


### -field DxFlipVideoPort

Points to the driver-supplied <a href="https://msdn.microsoft.com/d6047c90-1163-475a-a55b-95ccb0570e3e">DxFlipVideoPort</a> miniport driver callback function.


### -field DxGetPolarity

Points to the driver-supplied <a href="https://msdn.microsoft.com/9bce3093-8dcd-4e91-8e20-5558f2dcce75">DxGetPolarity</a> miniport driver callback function.


### -field DxGetCurrentAutoflip

Points to the driver-supplied <a href="https://msdn.microsoft.com/25010ffb-893f-401f-8883-f5a08e7014bf">DxGetCurrentAutoflip</a> miniport driver callback function.


### -field DxGetPreviousAutoflip

Points to the driver-supplied <a href="https://msdn.microsoft.com/3b19e4be-413c-4014-b414-cb2ba3e14b14">DxGetPreviousAutoflip</a> miniport driver callback function.


### -field DxTransfer

Points to the driver-supplied <a href="https://msdn.microsoft.com/62e1a5f6-9777-4acf-a531-b3554eaf89a6">DxTransfer</a> miniport driver callback function.


### -field DxGetTransferStatus

Points to the driver-supplied <a href="https://msdn.microsoft.com/e33ec8f0-2d1c-42cf-8b82-8f316f52e2a8">DxGetTransferStatus</a> miniport driver callback function.


## -see-also




<a href="https://msdn.microsoft.com/c4b38376-b54f-4fbb-b305-5951a1ea76a1">DxApi</a>
 

 

