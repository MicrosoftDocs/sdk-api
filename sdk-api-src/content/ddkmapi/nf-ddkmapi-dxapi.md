---
UID: NF:ddkmapi.DxApi
title: DxApi function
author: windows-driver-content
description: The DxApi function accepts commands from the hardware decoder's video capture driver to access the DxApi interface functions that are implemented in a video miniport driver.
old-location: display\dxapi.htm
old-project: display
ms.assetid: c4b38376-b54f-4fbb-b305-5951a1ea76a1
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: DxApi, DxApi function [Display Devices], ddfncs_b76158a1-30ff-4874-b527-a201c5a67fc5.xml, display.dxapi, dxapi/DxApi
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ddkmapi.h
req.include-header: Ddkmapi.h
req.target-type: Desktop
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
req.typenames: "*LPDDKERNELCAPS, DDKERNELCAPS"
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	LibDef
api_location:
-	Dxapi.lib
-	Dxapi.dll
api_name:
-	DxApi
product: Windows
targetos: Windows
req.lib: Dxapi.lib
req.dll: 
req.irql: 
---

# DxApi function


## -description


The <b>DxApi</b> function accepts commands from the hardware decoder's video capture driver to access the <a href="https://msdn.microsoft.com/cfe77d14-32d2-44b7-8121-20ae7e4fe79e">DxApi interface functions</a> that are implemented in a <a href="https://msdn.microsoft.com/3a540bfe-f340-4f12-acee-323b97683074">video miniport driver</a>.


## -parameters




### -param dwFunctionNum

Indicates the behavior of the <b>DxApi</b> function (function identifier). See the Remarks section for the list of function identifiers.


### -param lpvInBuffer

Points to the input buffer.


### -param cbInBuffer

Indicates the size in bytes of the input buffer.


### -param lpvOutBuffer

Points to the output buffer.


### -param cbOutBuffer

Indicates the size in bytes of the output buffer.


## -returns



<b>DxApi</b> returns the number of bytes actually written to the output buffer.




## -remarks



<b>DxApi</b> accepts a function identifier (<i>dwFunctionNum</i>), an input buffer (<i>lpvInBuffer</i>) and its size (<i>cbInBuffer</i>), and an output buffer (<i>lpvOutBuffer</i>) and its size (<i>cbOutBuffer</i>). The behavior of the function and the size and format of the input and output buffers depend on the specified function identifier. The return value is the number of actual bytes written into the output buffer.

The following function identifiers are defined for the <b>DxApi</b> function in the <i>ddkmapi.h</i> header file: 


<a href="https://msdn.microsoft.com/library/windows/hardware/ff550599">DD_DXAPI_ADDVPCAPTUREBUFFER</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550606">DD_DXAPI_CLOSEHANDLE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550612">DD_DXAPI_FLIP_OVERLAY</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550618">DD_DXAPI_FLIP_VP</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550622">DD_DXAPI_FLUSHVPCAPTUREBUFFERS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550642">DD_DXAPI_GET_CURRENT_VP_AUTOFLIP_SURFACE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550650">DD_DXAPI_GET_LAST_VP_AUTOFLIP_SURFACE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550660">DD_DXAPI_GET_POLARITY</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550673">DD_DXAPI_GET_SURFACE_STATE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550686">DD_DXAPI_GET_VP_FIELD_NUMBER</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550629">DD_DXAPI_GETKERNELCAPS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550637">DD_DXAPI_GETVERSIONNUMBER</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550695">DD_DXAPI_LOCK</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550702">DD_DXAPI_OPENDIRECTDRAW</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550711">DD_DXAPI_OPENSURFACE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551498">DD_DXAPI_OPENVIDEOPORT</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551500">DD_DXAPI_OPENVPCAPTUREDEVICE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551502">DD_DXAPI_REGISTER_CALLBACK</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551504">DD_DXAPI_SET_SURFACE_STATE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551507">DD_DXAPI_SET_VP_FIELD_NUMBER</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551510">DD_DXAPI_SET_VP_SKIP_FIELD</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551514">DD_DXAPI_UNREGISTER_CALLBACK</a>





## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550599">DD_DXAPI_ADDVPCAPTUREBUFFER</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550606">DD_DXAPI_CLOSEHANDLE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550612">DD_DXAPI_FLIP_OVERLAY</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550618">DD_DXAPI_FLIP_VP</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550622">DD_DXAPI_FLUSHVPCAPTUREBUFFERS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550629">DD_DXAPI_GETKERNELCAPS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550637">DD_DXAPI_GETVERSIONNUMBER</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550642">DD_DXAPI_GET_CURRENT_VP_AUTOFLIP_SURFACE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550650">DD_DXAPI_GET_LAST_VP_AUTOFLIP_SURFACE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550660">DD_DXAPI_GET_POLARITY</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550673">DD_DXAPI_GET_SURFACE_STATE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550686">DD_DXAPI_GET_VP_FIELD_NUMBER</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550695">DD_DXAPI_LOCK</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550702">DD_DXAPI_OPENDIRECTDRAW</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550711">DD_DXAPI_OPENSURFACE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551498">DD_DXAPI_OPENVIDEOPORT</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551500">DD_DXAPI_OPENVPCAPTUREDEVICE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551502">DD_DXAPI_REGISTER_CALLBACK</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551504">DD_DXAPI_SET_SURFACE_STATE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551507">DD_DXAPI_SET_VP_FIELD_NUMBER</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551510">DD_DXAPI_SET_VP_SKIP_FIELD</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551514">DD_DXAPI_UNREGISTER_CALLBACK</a>
 

 

