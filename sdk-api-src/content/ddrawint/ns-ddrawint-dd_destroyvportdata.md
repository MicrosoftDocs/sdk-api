---
UID: NS:ddrawint._DD_DESTROYVPORTDATA
title: DD_DESTROYVPORTDATA (ddrawint.h)
description: The DD_DESTROYVPORTDATA structure contains the information necessary for the driver to clean up.
helpviewer_keywords: ["*PDD_DESTROYVPORTDATA","DD_DESTROYVPORTDATA","DD_DESTROYVPORTDATA structure [Display Devices]","ddrawint/DD_DESTROYVPORTDATA","ddstrcts_bb54464c-6b2f-4c90-99a9-439938562898.xml","display.dd_destroyvportdata"]
old-location: display\dd_destroyvportdata.htm
tech.root: display
ms.assetid: b9e29c23-bb1a-47e8-a605-2863c4cda2af
ms.date: 12/05/2018
ms.keywords: '*PDD_DESTROYVPORTDATA, DD_DESTROYVPORTDATA, DD_DESTROYVPORTDATA structure [Display Devices], ddrawint/DD_DESTROYVPORTDATA, ddstrcts_bb54464c-6b2f-4c90-99a9-439938562898.xml, display.dd_destroyvportdata'
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
req.typenames: '*PDD_DESTROYVPORTDATA, DD_DESTROYVPORTDATA'
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DD_DESTROYVPORTDATA
 - ddrawint/_DD_DESTROYVPORTDATA
 - PDD_DESTROYVPORTDATA
 - ddrawint/PDD_DESTROYVPORTDATA
 - DD_DESTROYVPORTDATA
 - ddrawint/DD_DESTROYVPORTDATA
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
 - DD_DESTROYVPORTDATA
---

# DD_DESTROYVPORTDATA structure


## -description

The DD_DESTROYVPORTDATA structure contains the information necessary for the driver to clean up.

## -struct-fields

### -field lpDD

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_directdraw_local">DD_DIRECTDRAW_LOCAL</a> structure that is relevant to the current Microsoft DirectDraw process only.

### -field lpVideoPort

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_videoport_local">DD_VIDEOPORT_LOCAL</a> structure that represents this <a href="/windows-hardware/drivers/">video port extensions (VPE)</a> object.

### -field ddRVal

Specifies the location in which the driver writes the return value of the <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_vportcb_destroyvport">DdVideoPortDestroy</a> callback. A return code of DD_OK indicates success. For more information, see <a href="/windows-hardware/drivers/display/return-values-for-directdraw">Return Values for DirectDraw</a>.

### -field DestroyVideoPort

Used by the DirectDraw API and should not be filled in by the driver.

## -see-also

<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_vportcb_destroyvport">DdVideoPortDestroy</a>