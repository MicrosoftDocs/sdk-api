---
UID: NS:ddrawint._DD_CREATEVPORTDATA
title: DD_CREATEVPORTDATA (ddrawint.h)
author: windows-sdk-content
description: The DD_CREATEVPORTDATA structure contains the information necessary to describe the video port extensions (VPE) object being created.
old-location: display\dd_createvportdata.htm
tech.root: display
ms.assetid: c4dea564-399a-46ee-ad71-7a374d6fbc0a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: '*PDD_CREATEVPORTDATA, DD_CREATEVPORTDATA, DD_CREATEVPORTDATA structure [Display Devices], ddrawint/DD_CREATEVPORTDATA, ddstrcts_397bd4aa-7d61-4efa-b47e-1ec97556a429.xml, display.dd_createvportdata'
ms.topic: struct
f1_keywords:
- ddrawint/DD_CREATEVPORTDATA
req.header: ddrawint.h
req.include-header: Winddi.h
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
- ddrawint.h
api_name:
- DD_CREATEVPORTDATA
product: Windows
targetos: Windows
req.typenames: '*PDD_CREATEVPORTDATA, DD_CREATEVPORTDATA'
req.redist: 
ms.custom: 19H1
---

# DD_CREATEVPORTDATA structure


## -description


The DD_CREATEVPORTDATA structure contains the information necessary to describe the <a href="https://docs.microsoft.com/windows-hardware/drivers/">video port extensions (VPE)</a> object being created.


## -struct-fields




### -field lpDD

Points to a <a href="https://docs.microsoft.com/windows/desktop/api/ddrawint/ns-ddrawint-dd_directdraw_local">DD_DIRECTDRAW_LOCAL</a> structure that is relevant to the current Microsoft DirectDraw process only.


### -field lpDDVideoPortDesc

Points to a <a href="https://docs.microsoft.com/windows/desktop/api/dvp/ns-dvp-ddvideoportdesc">DDVIDEOPORTDESC</a> structure that describes the created VPE object.


### -field lpVideoPort

Points to a <a href="https://docs.microsoft.com/windows/desktop/api/ddrawint/ns-ddrawint-dd_videoport_local">DD_VIDEOPORT_LOCAL</a> structure that represents the created VPE object.


### -field ddRVal

Specifies the location in which the driver writes the return value of the <a href="https://docs.microsoft.com/windows/desktop/api/ddrawint/nc-ddrawint-pdd_vportcb_createvideoport">DdVideoPortCreate</a> callback. A return code of DD_OK indicates success. For more information, see <a href="https://docs.microsoft.com/windows-hardware/drivers/display/return-values-for-directdraw">Return Values for DirectDraw</a>.


### -field CreateVideoPort

Used by the DirectDraw API and should not be filled in by the driver. 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ddrawint/nc-ddrawint-pdd_vportcb_createvideoport">DdVideoPortCreate</a>
 

 

