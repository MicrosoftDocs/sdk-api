---
UID: NC:ddrawint.PDD_VPORTCB_CANCREATEVIDEOPORT
title: PDD_VPORTCB_CANCREATEVIDEOPORT (ddrawint.h)
description: The DdVideoPortCanCreate callback function determines whether the driver can support a DirectDraw VPE object of the specified description.
helpviewer_keywords: ["DdVideoPortCanCreate","DdVideoPortCanCreate callback function [Display Devices]","PDD_VPORTCB_CANCREATEVIDEOPORT","PDD_VPORTCB_CANCREATEVIDEOPORT callback","ddfncs_dfe3285f-627c-4f0d-b7e7-ffd87d88fe46.xml","ddrawint/DdVideoPortCanCreate","display.ddvideoportcancreate"]
old-location: display\ddvideoportcancreate.htm
tech.root: display
ms.assetid: 742c7af2-0611-4cca-b18c-e14b18068d7e
ms.date: 12/05/2018
ms.keywords: DdVideoPortCanCreate, DdVideoPortCanCreate callback function [Display Devices], PDD_VPORTCB_CANCREATEVIDEOPORT, PDD_VPORTCB_CANCREATEVIDEOPORT callback, ddfncs_dfe3285f-627c-4f0d-b7e7-ffd87d88fe46.xml, ddrawint/DdVideoPortCanCreate, display.ddvideoportcancreate
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
 - PDD_VPORTCB_CANCREATEVIDEOPORT
 - ddrawint/PDD_VPORTCB_CANCREATEVIDEOPORT
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
 - DdVideoPortCanCreate
---

## -description

The <i>DdVideoPortCanCreate</i> callback function determines whether the driver can support a DirectDraw VPE object of the specified description.

## -parameters

### -param unnamedParam1

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_cancreatevportdata">DD_CANCREATEVPORTDATA</a> structure that contains the information necessary for the driver to determine whether the specified DirectDraw VPE object can be supported.

## -returns

<i>DdVideoPortCanCreate</i> returns one of the following callback codes:

## -remarks

<i>DdVideoPortCanCreate</i> must be implemented in drivers that support VPE.

The driver should check the members of the <a href="/windows/desktop/api/dvp/ns-dvp-ddvideoportdesc">DDVIDEOPORTDESC</a> structure to which the <b>lpDDVideoPortDesc</b> member of the DD_CANCREATEVPORTDATA structure at <i>lpCanCreateVideoPort</i> points to determine whether the hardware supports the specified type of VPE object.

## -see-also

<a href="/windows/desktop/api/dvp/ns-dvp-ddvideoportdesc">DDVIDEOPORTDESC</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_cancreatevportdata">DD_CANCREATEVPORTDATA</a>



<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_vportcb_createvideoport">DdVideoPortCreate</a>