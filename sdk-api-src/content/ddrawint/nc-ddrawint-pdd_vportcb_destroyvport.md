---
UID: NC:ddrawint.PDD_VPORTCB_DESTROYVPORT
title: PDD_VPORTCB_DESTROYVPORT
author: windows-sdk-content
description: The DdVideoPortDestroy callback function notifies the driver that DirectDraw has destroyed the specified VPE object.
old-location: display\ddvideoportdestroy.htm
tech.root: display
ms.assetid: 0426eeaa-4d9a-4e5e-8550-2f7adbb26685
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: DdVideoPortDestroy, DdVideoPortDestroy callback function [Display Devices], PDD_VPORTCB_DESTROYVPORT, PDD_VPORTCB_DESTROYVPORT callback, ddfncs_865d04b1-c817-4000-9fdc-9e498dee679c.xml, ddrawint/DdVideoPortDestroy, display.ddvideoportdestroy
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: ddrawint.h
req.include-header: Winddi.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - ddrawint.h
api_name:
 - DdVideoPortDestroy
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PDD_VPORTCB_DESTROYVPORT callback function


## -description


The <b>DdVideoPortDestroy</b> callback function notifies the driver that DirectDraw has destroyed the specified VPE object.


## -parameters




### -param Arg1








#### - lpDestroyVideoPort

Points to a <a href="https://msdn.microsoft.com/b9e29c23-bb1a-47e8-a605-2863c4cda2af">DD_DESTROYVPORTDATA</a> structure that contains the information required for the driver to clean up.


## -returns



<b>DdVideoPortDestroy</b> returns one of the following callback codes:




## -remarks



<b>DdVideoPortDestroy</b> can be optionally implemented in DirectDraw drivers that support VPE.

The driver should free any memory that it allocated and associated with the specified VPE object. This includes freeing any driver-allocated memory accessed through the <b>dwReserved1</b> and <b>dwReserved2</b> members of the <a href="https://msdn.microsoft.com/c497d1ef-0eb1-465f-978c-60cf5606de93">DD_VIDEOPORT_LOCAL</a> structure. This DD_VIDEOPORT_LOCAL structure is at the <b>lpVideoPort</b> member of the DD_DESTROYVPORTDATA structure at <i>lpDestroyVideoPort</i>. 




## -see-also




<a href="https://msdn.microsoft.com/b9e29c23-bb1a-47e8-a605-2863c4cda2af">DD_DESTROYVPORTDATA</a>



<a href="https://msdn.microsoft.com/c497d1ef-0eb1-465f-978c-60cf5606de93">DD_VIDEOPORT_LOCAL</a>



<a href="https://msdn.microsoft.com/eeaf3cda-6220-4e8e-8f9e-9f52d1b05ab7">DdVideoPortCreate</a>
 

 

