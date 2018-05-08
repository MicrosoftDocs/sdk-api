---
UID: NS:vmr9._VMR9ProcAmpControlRange
title: "_VMR9ProcAmpControlRange"
author: windows-driver-content
description: The VMR9ProcAmpControlRange structure specifies the valid range for an image adjustment property. The range depends on the graphics device driver. This structure is used with the Video Mixing Renderer 9 Filter (VMR-9).
old-location: dshow\vmr9procampcontrolrange.htm
old-project: DirectShow
ms.assetid: 5fa61ed8-4fd6-42fb-8c5b-87d23e239cd1
ms.author: windowsdriverdev
ms.date: 4/30/2018
ms.keywords: VMR9ProcAmpControlRange, VMR9ProcAmpControlRange structure [DirectShow], VMR9ProcAmpControlRangeStructure, _VMR9ProcAmpControlRange, dshow.vmr9procampcontrolrange, vmr9/VMR9ProcAmpControlRange
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: vmr9.h
req.include-header: 
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
req.typenames: VMR9ProcAmpControlRange
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Vmr9.h
api_name:
-	VMR9ProcAmpControlRange
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# _VMR9ProcAmpControlRange structure


## -description



The <code>VMR9ProcAmpControlRange</code> structure specifies the valid range for an image adjustment property. The range depends on the graphics device driver. This structure is used with the Video Mixing Renderer 9 Filter (VMR-9).




## -struct-fields




### -field dwSize

Size of the structure, in bytes. The value must be <code>sizeof(VMR9ProcAmpControlRange)</code>.


### -field dwProperty

Specifies the image adjustment property to query, as a member of the <a href="https://msdn.microsoft.com/5dfba718-4c89-46e7-89b6-e4b133b0ce04">VMR9ProcAmpControlFlags</a> enumeration. The caller should set this field.


### -field MinValue

Specifies the minimum value for the property. The driver sets this field.


### -field MaxValue

Specifies the maximum value for the property. The driver sets this field.


### -field DefaultValue

Specifies the default value for the property. The default value is the value that does not alter the image. The driver sets this field.


### -field StepSize

Specifies the valid increments from <b>MinValue</b> to <b>MaxValue</b>. The driver sets this field.


## -see-also




<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>



<a href="https://msdn.microsoft.com/e7db2b22-b3d2-4c6f-84fc-5a287761ed7a">IVMRMixerControl9::GetProcAmpControlRange</a>
 

 

