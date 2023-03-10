---
UID: NE:iketypes.IKEEXT_MM_SA_STATE_
title: IKEEXT_MM_SA_STATE (iketypes.h)
description: States for the Main Mode (MM) negotiation exchanges that are part of the Authenticated Internet Protocol (AuthIP) and Internet Key Exchange (IKE) protocols.
helpviewer_keywords: ["IKEEXT_MM_SA_STATE","IKEEXT_MM_SA_STATE enumeration [Filtering]","IKEEXT_MM_SA_STATE_COMPLETE","IKEEXT_MM_SA_STATE_FINAL","IKEEXT_MM_SA_STATE_FINAL_SENT","IKEEXT_MM_SA_STATE_MAX","IKEEXT_MM_SA_STATE_NONE","IKEEXT_MM_SA_STATE_SA_SENT","IKEEXT_MM_SA_STATE_SSPI_SENT","fwp.ikeext_mm_sa_state","iketypes/IKEEXT_MM_SA_STATE","iketypes/IKEEXT_MM_SA_STATE_COMPLETE","iketypes/IKEEXT_MM_SA_STATE_FINAL","iketypes/IKEEXT_MM_SA_STATE_FINAL_SENT","iketypes/IKEEXT_MM_SA_STATE_MAX","iketypes/IKEEXT_MM_SA_STATE_NONE","iketypes/IKEEXT_MM_SA_STATE_SA_SENT","iketypes/IKEEXT_MM_SA_STATE_SSPI_SENT"]
old-location: fwp\ikeext_mm_sa_state.htm
tech.root: fwp
ms.assetid: 5af48053-23b7-489f-82b7-743153aea641
ms.date: 12/05/2018
ms.keywords: IKEEXT_MM_SA_STATE, IKEEXT_MM_SA_STATE enumeration [Filtering], IKEEXT_MM_SA_STATE_COMPLETE, IKEEXT_MM_SA_STATE_FINAL, IKEEXT_MM_SA_STATE_FINAL_SENT, IKEEXT_MM_SA_STATE_MAX, IKEEXT_MM_SA_STATE_NONE, IKEEXT_MM_SA_STATE_SA_SENT, IKEEXT_MM_SA_STATE_SSPI_SENT, fwp.ikeext_mm_sa_state, iketypes/IKEEXT_MM_SA_STATE, iketypes/IKEEXT_MM_SA_STATE_COMPLETE, iketypes/IKEEXT_MM_SA_STATE_FINAL, iketypes/IKEEXT_MM_SA_STATE_FINAL_SENT, iketypes/IKEEXT_MM_SA_STATE_MAX, iketypes/IKEEXT_MM_SA_STATE_NONE, iketypes/IKEEXT_MM_SA_STATE_SA_SENT, iketypes/IKEEXT_MM_SA_STATE_SSPI_SENT
req.header: iketypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: IKEEXT_MM_SA_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IKEEXT_MM_SA_STATE_
 - iketypes/IKEEXT_MM_SA_STATE_
 - IKEEXT_MM_SA_STATE
 - iketypes/IKEEXT_MM_SA_STATE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iketypes.h
api_name:
 - IKEEXT_MM_SA_STATE
---

# IKEEXT_MM_SA_STATE enumeration


## -description

The <b>IKEEXT_MM_SA_STATE</b> enumerated type defines the states for the Main Mode (MM) negotiation exchanges that are part of the Authenticated Internet Protocol (AuthIP) and Internet Key Exchange (IKE) protocols.

## -enum-fields

### -field IKEEXT_MM_SA_STATE_NONE:0

Initial state.  No packets have been sent to the peer.

### -field IKEEXT_MM_SA_STATE_SA_SENT

First packet has been sent to the peer

### -field IKEEXT_MM_SA_STATE_SSPI_SENT

Second packet has been sent to the peer, for SSPI authentication.

### -field IKEEXT_MM_SA_STATE_FINAL

Third packet has been sent to the peer.

### -field IKEEXT_MM_SA_STATE_FINAL_SENT

Final packet has been sent to the peer.

### -field IKEEXT_MM_SA_STATE_COMPLETE

MM has been completed.

### -field IKEEXT_MM_SA_STATE_MAX

Maximum value for testing purposes.

## -see-also

<a href="/windows/desktop/FWP/fwp-enums">Windows Filtering Platform API Enumerated Types</a>
