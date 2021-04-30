---
UID: NC:ddrawint.PDD_VPORTCB_CREATEVIDEOPORT
title: PDD_VPORTCB_CREATEVIDEOPORT (ddrawint.h)
description: The DdVideoPortCreate callback function notifies the driver that DirectDraw has created a VPE object.
helpviewer_keywords: ["DdVideoPortCreate","DdVideoPortCreate callback function [Display Devices]","PDD_VPORTCB_CREATEVIDEOPORT","PDD_VPORTCB_CREATEVIDEOPORT callback","ddfncs_abbd3ac5-70a9-40ff-a22d-42c49eda1c96.xml","ddrawint/DdVideoPortCreate","display.ddvideoportcreate"]
old-location: display\ddvideoportcreate.htm
tech.root: display
ms.assetid: eeaf3cda-6220-4e8e-8f9e-9f52d1b05ab7
ms.date: 12/05/2018
ms.keywords: DdVideoPortCreate, DdVideoPortCreate callback function [Display Devices], PDD_VPORTCB_CREATEVIDEOPORT, PDD_VPORTCB_CREATEVIDEOPORT callback, ddfncs_abbd3ac5-70a9-40ff-a22d-42c49eda1c96.xml, ddrawint/DdVideoPortCreate, display.ddvideoportcreate
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PDD_VPORTCB_CREATEVIDEOPORT
 - ddrawint/PDD_VPORTCB_CREATEVIDEOPORT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - ddrawint.h
api_name:
 - DdVideoPortCreate
---

## -description

The <b>DdVideoPortCreate</b> callback function notifies the driver that DirectDraw has created a VPE object.

## -parameters

### -param unnamedParam1

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_createvportdata">DD_CREATEVPORTDATA</a> structure that describes the created VPE object.

## -returns

<b>DdVideoPortCreate</b> returns one of the following values:

## -remarks

<b>DdVideoPortCreate</b> can be optionally implemented in DirectDraw drivers that support VPE.

<b>DdVideoPortCreate</b> can allocate memory for and initialize any private, VPE object-specific data. The driver can use the <b>dwReserved1</b> and <b>dwReserved2</b> members of the <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_videoport_local">DD_VIDEOPORT_LOCAL</a> structure to store this data. This DD_VIDEOPORT_LOCAL structure is at the <b>lpVideoPort</b> member of the DD_CREATEVPORTDATA structure at <i>lpCreateVideoPort</i>. The driver cannot use or change any other members of the DD_VIDEOPORT_LOCAL structure.

If the hardware video port is implemented to use the feature connector, the driver might need to initialize the feature connector for hardware video port use.

<b>DdVideoPortCreate</b> should not turn the hardware video port on. This is accomplished in <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_vportcb_update">DdVideoPortUpdate</a>.

## -see-also

<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_createvportdata">DD_CREATEVPORTDATA</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_videoport_local">DD_VIDEOPORT_LOCAL</a>



<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_vportcb_update">DdVideoPortUpdate</a>