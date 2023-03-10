---
UID: NE:iketypes.IKEEXT_EM_SA_STATE_
title: IKEEXT_EM_SA_STATE (iketypes.h)
description: States for the Extended Mode (EM) negotiation exchanges that are part of the Authenticated Internet Protocol (AuthIP) protocol.
helpviewer_keywords: ["IKEEXT_EM_SA_STATE","IKEEXT_EM_SA_STATE enumeration [Filtering]","IKEEXT_EM_SA_STATE_AUTH_COMPLETE","IKEEXT_EM_SA_STATE_COMPLETE","IKEEXT_EM_SA_STATE_FINAL","IKEEXT_EM_SA_STATE_MAX","IKEEXT_EM_SA_STATE_NONE","IKEEXT_EM_SA_STATE_SENT_ATTS","IKEEXT_EM_SA_STATE_SSPI_SENT","fwp.ikeext_em_sa_state","iketypes/IKEEXT_EM_SA_STATE","iketypes/IKEEXT_EM_SA_STATE_AUTH_COMPLETE","iketypes/IKEEXT_EM_SA_STATE_COMPLETE","iketypes/IKEEXT_EM_SA_STATE_FINAL","iketypes/IKEEXT_EM_SA_STATE_MAX","iketypes/IKEEXT_EM_SA_STATE_NONE","iketypes/IKEEXT_EM_SA_STATE_SENT_ATTS","iketypes/IKEEXT_EM_SA_STATE_SSPI_SENT"]
old-location: fwp\ikeext_em_sa_state.htm
tech.root: fwp
ms.assetid: 378b4a24-4a31-4e9e-83f2-aec9266d1a94
ms.date: 12/05/2018
ms.keywords: IKEEXT_EM_SA_STATE, IKEEXT_EM_SA_STATE enumeration [Filtering], IKEEXT_EM_SA_STATE_AUTH_COMPLETE, IKEEXT_EM_SA_STATE_COMPLETE, IKEEXT_EM_SA_STATE_FINAL, IKEEXT_EM_SA_STATE_MAX, IKEEXT_EM_SA_STATE_NONE, IKEEXT_EM_SA_STATE_SENT_ATTS, IKEEXT_EM_SA_STATE_SSPI_SENT, fwp.ikeext_em_sa_state, iketypes/IKEEXT_EM_SA_STATE, iketypes/IKEEXT_EM_SA_STATE_AUTH_COMPLETE, iketypes/IKEEXT_EM_SA_STATE_COMPLETE, iketypes/IKEEXT_EM_SA_STATE_FINAL, iketypes/IKEEXT_EM_SA_STATE_MAX, iketypes/IKEEXT_EM_SA_STATE_NONE, iketypes/IKEEXT_EM_SA_STATE_SENT_ATTS, iketypes/IKEEXT_EM_SA_STATE_SSPI_SENT
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
req.typenames: IKEEXT_EM_SA_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IKEEXT_EM_SA_STATE_
 - iketypes/IKEEXT_EM_SA_STATE_
 - IKEEXT_EM_SA_STATE
 - iketypes/IKEEXT_EM_SA_STATE
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
 - IKEEXT_EM_SA_STATE
---

# IKEEXT_EM_SA_STATE enumeration


## -description

The <b>IKEEXT_EM_SA_STATE</b> enumerated type defines the states for the Extended Mode (EM) negotiation exchanges that are part of the Authenticated Internet Protocol (AuthIP) protocol.

## -enum-fields

### -field IKEEXT_EM_SA_STATE_NONE:0

Initial state.  No Extended Mode packets have been sent to the peer.

### -field IKEEXT_EM_SA_STATE_SENT_ATTS

First packet has been sent to the peer.

### -field IKEEXT_EM_SA_STATE_SSPI_SENT

Second packet has been sent to the peer.

### -field IKEEXT_EM_SA_STATE_AUTH_COMPLETE

Third packet has been sent to the peer.

### -field IKEEXT_EM_SA_STATE_FINAL

Final packet has been sent to the peer.

### -field IKEEXT_EM_SA_STATE_COMPLETE

Extended mode has been completed.

### -field IKEEXT_EM_SA_STATE_MAX

Maximum value for testing purposes.

## -see-also

<a href="/windows/desktop/FWP/fwp-enums">Windows Filtering Platform API Enumerated Types</a>
