---
UID: NE:dxva9typ._COPP_StatusHDCPFlags
title: COPP_StatusHDCPFlags (dxva9typ.h)
description: Contains HDCP status flags. This enumeration is used in the DXVA_COPPStatusHDCPKeyData structure.
helpviewer_keywords: ["COPP_HDCPFlagsReserved","COPP_HDCPRepeater","COPP_StatusHDCPFlags","COPP_StatusHDCPFlags","COPP_StatusHDCPFlags enumeration [DirectShow]","COPP_StatusHDCPFlagsEnumeration","dshow.copp_statushdcpflags","dxva9typ/COPP_HDCPFlagsReserved","dxva9typ/COPP_HDCPRepeater","dxva9typ/COPP_StatusHDCPFlags"]
old-location: dshow\copp_statushdcpflags.htm
tech.root: dshow
ms.assetid: 40ad7f00-9b4f-4c2d-8c6b-05725a072bfc
ms.date: 12/05/2018
ms.keywords: COPP_HDCPFlagsReserved, COPP_HDCPRepeater, COPP_StatusHDCPFlags, COPP_StatusHDCPFlags , COPP_StatusHDCPFlags enumeration [DirectShow], COPP_StatusHDCPFlagsEnumeration, dshow.copp_statushdcpflags, dxva9typ/COPP_HDCPFlagsReserved, dxva9typ/COPP_HDCPRepeater, dxva9typ/COPP_StatusHDCPFlags
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
req.typenames: COPP_StatusHDCPFlags
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _COPP_StatusHDCPFlags
 - dxva9typ/_COPP_StatusHDCPFlags
 - COPP_StatusHDCPFlags
 - dxva9typ/COPP_StatusHDCPFlags
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
 - COPP_StatusHDCPFlags
---

# COPP_StatusHDCPFlags enumeration


## -description

Contains HDCP status flags. This enumeration is used in the <a href="/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatushdcpkeydata">DXVA_COPPStatusHDCPKeyData</a> structure.

## -enum-fields

### -field COPP_HDCPRepeater:0x01

The device is an HDCP repeater.

### -field COPP_HDCPFlagsReserved:0xFFFFFFFE

Reserved. Must be zero.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>



<a href="/windows/desktop/DirectShow/using-certified-output-protection-protocol--copp">Using Certified Output Protection Protocol (COPP)</a>
