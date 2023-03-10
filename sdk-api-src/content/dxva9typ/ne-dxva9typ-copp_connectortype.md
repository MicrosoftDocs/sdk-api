---
UID: NE:dxva9typ._COPP_ConnectorType
title: COPP_ConnectorType (dxva9typ.h)
description: Specifies the type of physical connector.
helpviewer_keywords: ["COPP_ConnectorType","COPP_ConnectorType","COPP_ConnectorType enumeration [DirectShow]","COPP_ConnectorTypeEnumeration","COPP_ConnectorType_ComponentVideo","COPP_ConnectorType_CompositeVideo","COPP_ConnectorType_DVI","COPP_ConnectorType_D_JPN","COPP_ConnectorType_DisplayPortEmbedded","COPP_ConnectorType_DisplayPortExternal","COPP_ConnectorType_ForceDWORD","COPP_ConnectorType_HDMI","COPP_ConnectorType_Internal","COPP_ConnectorType_LVDS","COPP_ConnectorType_SDI","COPP_ConnectorType_SVideo","COPP_ConnectorType_TMDS","COPP_ConnectorType_UDIEmbedded","COPP_ConnectorType_UDIExternal","COPP_ConnectorType_Unknown","COPP_ConnectorType_VGA","dshow.copp_connectortype","dxva9typ/COPP_ConnectorType","dxva9typ/COPP_ConnectorType_ComponentVideo","dxva9typ/COPP_ConnectorType_CompositeVideo","dxva9typ/COPP_ConnectorType_DVI","dxva9typ/COPP_ConnectorType_D_JPN","dxva9typ/COPP_ConnectorType_DisplayPortEmbedded","dxva9typ/COPP_ConnectorType_DisplayPortExternal","dxva9typ/COPP_ConnectorType_ForceDWORD","dxva9typ/COPP_ConnectorType_HDMI","dxva9typ/COPP_ConnectorType_Internal","dxva9typ/COPP_ConnectorType_LVDS","dxva9typ/COPP_ConnectorType_SDI","dxva9typ/COPP_ConnectorType_SVideo","dxva9typ/COPP_ConnectorType_TMDS","dxva9typ/COPP_ConnectorType_UDIEmbedded","dxva9typ/COPP_ConnectorType_UDIExternal","dxva9typ/COPP_ConnectorType_Unknown","dxva9typ/COPP_ConnectorType_VGA"]
old-location: dshow\copp_connectortype.htm
tech.root: dshow
ms.assetid: 318603fa-a220-4c96-bd80-610d88e22bbd
ms.date: 12/05/2018
ms.keywords: COPP_ConnectorType, COPP_ConnectorType , COPP_ConnectorType enumeration [DirectShow], COPP_ConnectorTypeEnumeration, COPP_ConnectorType_ComponentVideo, COPP_ConnectorType_CompositeVideo, COPP_ConnectorType_DVI, COPP_ConnectorType_D_JPN, COPP_ConnectorType_DisplayPortEmbedded, COPP_ConnectorType_DisplayPortExternal, COPP_ConnectorType_ForceDWORD, COPP_ConnectorType_HDMI, COPP_ConnectorType_Internal, COPP_ConnectorType_LVDS, COPP_ConnectorType_SDI, COPP_ConnectorType_SVideo, COPP_ConnectorType_TMDS, COPP_ConnectorType_UDIEmbedded, COPP_ConnectorType_UDIExternal, COPP_ConnectorType_Unknown, COPP_ConnectorType_VGA, dshow.copp_connectortype, dxva9typ/COPP_ConnectorType, dxva9typ/COPP_ConnectorType_ComponentVideo, dxva9typ/COPP_ConnectorType_CompositeVideo, dxva9typ/COPP_ConnectorType_DVI, dxva9typ/COPP_ConnectorType_D_JPN, dxva9typ/COPP_ConnectorType_DisplayPortEmbedded, dxva9typ/COPP_ConnectorType_DisplayPortExternal, dxva9typ/COPP_ConnectorType_ForceDWORD, dxva9typ/COPP_ConnectorType_HDMI, dxva9typ/COPP_ConnectorType_Internal, dxva9typ/COPP_ConnectorType_LVDS, dxva9typ/COPP_ConnectorType_SDI, dxva9typ/COPP_ConnectorType_SVideo, dxva9typ/COPP_ConnectorType_TMDS, dxva9typ/COPP_ConnectorType_UDIEmbedded, dxva9typ/COPP_ConnectorType_UDIExternal, dxva9typ/COPP_ConnectorType_Unknown, dxva9typ/COPP_ConnectorType_VGA
req.header: dxva9typ.h
req.include-header: Dxva.h
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
req.typenames: COPP_ConnectorType
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _COPP_ConnectorType
 - dxva9typ/_COPP_ConnectorType
 - COPP_ConnectorType
 - dxva9typ/COPP_ConnectorType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxva9typ.h
api_name:
 - COPP_ConnectorType
---

## -description

Specifies the type of physical connector.

## -enum-fields

### -field COPP_ConnectorType_Unknown:-1

Unknown connector type.

### -field COPP_ConnectorType_VGA:0

VGA (Video Graphics Array) connector.

### -field COPP_ConnectorType_SVideo:1

S-Video connector.

### -field COPP_ConnectorType_CompositeVideo:2

Composite video connector.

### -field COPP_ConnectorType_ComponentVideo:3

Component video connector.

### -field COPP_ConnectorType_DVI:4

DVI (digital video interface) connector.

### -field COPP_ConnectorType_HDMI:5

HDMI (high-definition multimedia interface) connector.

### -field COPP_ConnectorType_LVDS:6

LVDS (Low voltage differential signaling) connector.

### -field COPP_ConnectorType_TMDS:7

Reserved.

### -field COPP_ConnectorType_D_JPN:8

Japanese D connector. (Connector conforming to the EIAJ RC-5237 standard.)

### -field COPP_ConnectorType_Internal:0x80000000

Internal connector. This flag can be combined with the other flags. This flag indicates that the connection between the graphics adapter and the display device is permanent and not accessible to the user.

### -field COPP_ConnectorType_ForceDWORD

Reserved. Do not use.

## -remarks

If a connector is described as <i>embedded</i> or <i>integrated</i>, it implies that the connector  is internal. These connectors have "Embedded" in the name of the enumeration constant. 

Applications should ignore the <b>COPP_ConnectorType_Internal</b> flag and instead check for connector types with "Embedded" in the constant name.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>



<a href="/windows/desktop/DirectShow/using-certified-output-protection-protocol--copp">Using Certified Output Protection Protocol (COPP)</a>
