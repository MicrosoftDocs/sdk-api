---
UID: NS:ddrawint._DD_GETMOCOMPGUIDSDATA
title: DD_GETMOCOMPGUIDSDATA (ddrawint.h)
description: The DD_GETMOCOMPGUIDSDATA structure contains the motion compensation GUID information.
helpviewer_keywords: ["*PDD_GETMOCOMPGUIDSDATA","DD_GETMOCOMPGUIDSDATA","DD_GETMOCOMPGUIDSDATA structure [Display Devices]","ddrawint/DD_GETMOCOMPGUIDSDATA","ddstrcts_fb041d18-05e9-4ef4-bb69-6dedf60bec78.xml","display.dd_getmocompguidsdata"]
old-location: display\dd_getmocompguidsdata.htm
tech.root: display
ms.assetid: d1507771-c2bc-4d10-a49e-57a3b60ac604
ms.date: 12/05/2018
ms.keywords: '*PDD_GETMOCOMPGUIDSDATA, DD_GETMOCOMPGUIDSDATA, DD_GETMOCOMPGUIDSDATA structure [Display Devices], ddrawint/DD_GETMOCOMPGUIDSDATA, ddstrcts_fb041d18-05e9-4ef4-bb69-6dedf60bec78.xml, display.dd_getmocompguidsdata'
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
req.typenames: '*PDD_GETMOCOMPGUIDSDATA, DD_GETMOCOMPGUIDSDATA'
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DD_GETMOCOMPGUIDSDATA
 - ddrawint/_DD_GETMOCOMPGUIDSDATA
 - PDD_GETMOCOMPGUIDSDATA
 - ddrawint/PDD_GETMOCOMPGUIDSDATA
 - DD_GETMOCOMPGUIDSDATA
 - ddrawint/DD_GETMOCOMPGUIDSDATA
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
 - DD_GETMOCOMPGUIDSDATA
---

# DD_GETMOCOMPGUIDSDATA structure


## -description

The DD_GETMOCOMPGUIDSDATA structure contains the motion compensation GUID information.

## -struct-fields

### -field lpDD

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_directdraw_local">DD_DIRECTDRAW_LOCAL</a> structure that is relevant to the current Microsoft DirectDraw process only.

### -field dwNumGuids

Indicates the number of motion compensation GUIDs in <b>lpGuids</b>.

### -field lpGuids

Points to a list of GUIDs that describe the motion compensation processes being used. If <b>lpGuids</b> is <b>NULL</b>, the driver should set <b>dwNumGuids</b> to the number of GUIDs that it supports. Otherwise, it should fill <b>lpGuids</b> with the GUIDs that it supports and set the number in <b>dwNumGuids</b>.

### -field ddRVal

Specifies the location in which the driver writes the return value of the <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_mocompcb_getguids">DdMoCompGetGuids</a> callback. A return code of DD_OK indicates success. For more information, see <a href="/windows-hardware/drivers/display/return-values-for-directdraw">Return Values for DirectDraw</a>.

## -see-also

<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_mocompcb_getguids">DdMoCompGetGuids</a>