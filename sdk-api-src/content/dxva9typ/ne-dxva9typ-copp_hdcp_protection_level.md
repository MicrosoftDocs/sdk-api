---
UID: NE:dxva9typ._COPP_HDCP_Protection_Level
title: COPP_HDCP_Protection_Level (dxva9typ.h)
description: Specifies the HDCP protection level.
helpviewer_keywords: ["COPP_HDCP_ForceDWORD","COPP_HDCP_Level0","COPP_HDCP_Level1","COPP_HDCP_LevelMax","COPP_HDCP_LevelMin","COPP_HDCP_Protection_Level","COPP_HDCP_Protection_Level","COPP_HDCP_Protection_Level enumeration [DirectShow]","COPP_HDCP_Protection_LevelEnumeration","dshow.copp_hdcp_protection_level","dxva9typ/COPP_HDCP_ForceDWORD","dxva9typ/COPP_HDCP_Level0","dxva9typ/COPP_HDCP_Level1","dxva9typ/COPP_HDCP_LevelMax","dxva9typ/COPP_HDCP_LevelMin","dxva9typ/COPP_HDCP_Protection_Level"]
old-location: dshow\copp_hdcp_protection_level.htm
tech.root: dshow
ms.assetid: 902ea4c6-8eba-4bfd-b986-5e7a5a2a5971
ms.date: 12/05/2018
ms.keywords: COPP_HDCP_ForceDWORD, COPP_HDCP_Level0, COPP_HDCP_Level1, COPP_HDCP_LevelMax, COPP_HDCP_LevelMin, COPP_HDCP_Protection_Level, COPP_HDCP_Protection_Level , COPP_HDCP_Protection_Level enumeration [DirectShow], COPP_HDCP_Protection_LevelEnumeration, dshow.copp_hdcp_protection_level, dxva9typ/COPP_HDCP_ForceDWORD, dxva9typ/COPP_HDCP_Level0, dxva9typ/COPP_HDCP_Level1, dxva9typ/COPP_HDCP_LevelMax, dxva9typ/COPP_HDCP_LevelMin, dxva9typ/COPP_HDCP_Protection_Level
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
req.typenames: COPP_HDCP_Protection_Level
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _COPP_HDCP_Protection_Level
 - dxva9typ/_COPP_HDCP_Protection_Level
 - COPP_HDCP_Protection_Level
 - dxva9typ/COPP_HDCP_Protection_Level
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
 - COPP_HDCP_Protection_Level
---

# COPP_HDCP_Protection_Level enumeration


## -description

Specifies the HDCP protection level.

## -enum-fields

### -field COPP_HDCP_Level0:0

HDCP protection is not enabled. See Remarks.

### -field COPP_HDCP_LevelMin

Minimum HDCP level. Equivalent to <b>COPP_HDCP_Level0</b>.

### -field COPP_HDCP_Level1:1

HDCP is enabled.

### -field COPP_HDCP_LevelMax

Maximum HDCP level. Equivalent to <b>COPP_HDCP_Level1</b>.

### -field COPP_HDCP_ForceDWORD:0x7fffffff

Reserved.

## -remarks

Some televisions do not have robust support for switching HDCP protection on and off. Because of this limitation, the graphics driver might leave HDCP enabled when the application sets the protection level to zero. If the application sets the HDCP level to zero, therefore, it might receive a COPP status message indicating that HDCP is still enabled. This is not an error.

For more information about HDCP, see http://www.digital-cp.com/.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>



<a href="/windows/desktop/DirectShow/using-certified-output-protection-protocol--copp">Using Certified Output Protection Protocol (COPP)</a>
