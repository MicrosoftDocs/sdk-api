---
UID: NS:wingdi.tagEMRMODIFYWORLDTRANSFORM
title: tagEMRMODIFYWORLDTRANSFORM
author: windows-sdk-content
description: The EMRMODIFYWORLDTRANSFORM structure contains members for the ModifyWorldTransform enhanced metafile record.
old-location: gdi\emrmodifyworldtransform.htm
tech.root: gdi
ms.assetid: 61d51fc9-a8dd-4981-940d-eedc8936360a
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: "*PEMRMODIFYWORLDTRANSFORM, EMRMODIFYWORLDTRANSFORM, EMRMODIFYWORLDTRANSFORM structure [Windows GDI], PEMRMODIFYWORLDTRANSFORM, PEMRMODIFYWORLDTRANSFORM structure pointer [Windows GDI], _win32_EMRMODIFYWORLDTRANSFORM_str, gdi.emrmodifyworldtransform, tagEMRMODIFYWORLDTRANSFORM, wingdi/EMRMODIFYWORLDTRANSFORM, wingdi/PEMRMODIFYWORLDTRANSFORM"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - Wingdi.h
api_name:
 - EMRMODIFYWORLDTRANSFORM
product: Windows
targetos: Windows
req.typenames: EMRMODIFYWORLDTRANSFORM, *PEMRMODIFYWORLDTRANSFORM
req.redist: 
---

# tagEMRMODIFYWORLDTRANSFORM structure


## -description



The <b>EMRMODIFYWORLDTRANSFORM</b> structure contains members for the <a href="https://msdn.microsoft.com/2ce070e8-dd6d-4f28-8214-37e825b44273">ModifyWorldTransform</a> enhanced metafile record.




## -struct-fields




### -field emr

The base structure for all record types.


### -field xform

The world-space to page-space transform data.


### -field iMode

Indicates how the transformation data modifies the current world transformation. This member can be one of the following values: MWT_IDENTITY, MWT_LEFTMULTIPLY, or MWT_RIGHTMULTIPLY.


## -see-also




<a href="https://msdn.microsoft.com/06582047-b64b-44ec-ae27-1f8ed7c56b97">EMR</a>



<a href="https://msdn.microsoft.com/6a509ed5-cea3-4318-ad17-9d20425a6e80">Metafile Structures</a>



<a href="https://msdn.microsoft.com/309ee4cf-111b-4f09-a722-4823cb3d26b0">Metafiles Overview</a>



<a href="https://msdn.microsoft.com/2ce070e8-dd6d-4f28-8214-37e825b44273">ModifyWorldTransform</a>



<a href="https://msdn.microsoft.com/49f0d7ee-77fa-415e-af00-b8930253a3a9">XFORM</a>
 

 

