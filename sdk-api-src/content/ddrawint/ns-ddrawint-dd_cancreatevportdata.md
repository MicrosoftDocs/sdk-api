---
UID: NS:ddrawint._DD_CANCREATEVPORTDATA
title: DD_CANCREATEVPORTDATA (ddrawint.h)
description: The DD_CANCREATEVPORTDATA structure contains the information required for the driver to determine whether a video port extensions (VPE) object can be created.
helpviewer_keywords: ["*PDD_CANCREATEVPORTDATA","DD_CANCREATEVPORTDATA","DD_CANCREATEVPORTDATA structure [Display Devices]","ddrawint/DD_CANCREATEVPORTDATA","ddstrcts_72b44069-d635-4675-b632-d0d077aa96e8.xml","display.dd_cancreatevportdata"]
old-location: display\dd_cancreatevportdata.htm
tech.root: display
ms.assetid: 60116f1d-fca2-4282-95a9-2af8da113a20
ms.date: 12/05/2018
ms.keywords: '*PDD_CANCREATEVPORTDATA, DD_CANCREATEVPORTDATA, DD_CANCREATEVPORTDATA structure [Display Devices], ddrawint/DD_CANCREATEVPORTDATA, ddstrcts_72b44069-d635-4675-b632-d0d077aa96e8.xml, display.dd_cancreatevportdata'
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
targetos: Windows
req.typenames: '*PDD_CANCREATEVPORTDATA, DD_CANCREATEVPORTDATA'
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DD_CANCREATEVPORTDATA
 - ddrawint/_DD_CANCREATEVPORTDATA
 - PDD_CANCREATEVPORTDATA
 - ddrawint/PDD_CANCREATEVPORTDATA
 - DD_CANCREATEVPORTDATA
 - ddrawint/DD_CANCREATEVPORTDATA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ddrawint.h
api_name:
 - DD_CANCREATEVPORTDATA
---

# DD_CANCREATEVPORTDATA structure


## -description

The DD_CANCREATEVPORTDATA structure contains the information required for the driver to determine whether a <a href="/windows-hardware/drivers/">video port extensions (VPE)</a> object can be created.

## -struct-fields

### -field lpDD

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_directdraw_local">DD_DIRECTDRAW_LOCAL</a> structure that is relevant to the current Microsoft DirectDraw process only.

### -field lpDDVideoPortDesc

Points to a <a href="/windows/desktop/api/dvp/ns-dvp-ddvideoportdesc">DDVIDEOPORTDESC</a> structure that contains a description of the VPE object being requested.

### -field ddRVal

Specifies the location in which the driver writes the return value of the <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_vportcb_cancreatevideoport">DdVideoPortCanCreate</a> callback. A return code of DD_OK indicates success. For more information, see <a href="/windows-hardware/drivers/display/return-values-for-directdraw">Return Values for DirectDraw</a>.

### -field CanCreateVideoPort

Used by the DirectDraw API and should not be filled in by the driver.

## -see-also

<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_vportcb_cancreatevideoport">DdVideoPortCanCreate</a>