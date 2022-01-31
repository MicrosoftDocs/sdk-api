---
UID: NE:iketypes.IKEEXT_QM_SA_STATE_
title: IKEEXT_QM_SA_STATE (iketypes.h)
description: States for the Quick Mode (QM) negotiation exchanges that are part of the Authenticated Internet Protocol (AuthIP) and Internet Key Exchange (IKE) protocols.
helpviewer_keywords: ["IKEEXT_QM_SA_STATE","IKEEXT_QM_SA_STATE enumeration [Filtering]","IKEEXT_QM_SA_STATE_COMPLETE","IKEEXT_QM_SA_STATE_FINAL","IKEEXT_QM_SA_STATE_INITIAL","IKEEXT_QM_SA_STATE_MAX","IKEEXT_QM_SA_STATE_NONE","fwp.ikeext_qm_sa_state","iketypes/IKEEXT_QM_SA_STATE","iketypes/IKEEXT_QM_SA_STATE_COMPLETE","iketypes/IKEEXT_QM_SA_STATE_FINAL","iketypes/IKEEXT_QM_SA_STATE_INITIAL","iketypes/IKEEXT_QM_SA_STATE_MAX","iketypes/IKEEXT_QM_SA_STATE_NONE"]
old-location: fwp\ikeext_qm_sa_state.htm
tech.root: fwp
ms.assetid: e1124447-dd56-4ab6-affc-59e351407261
ms.date: 12/05/2018
ms.keywords: IKEEXT_QM_SA_STATE, IKEEXT_QM_SA_STATE enumeration [Filtering], IKEEXT_QM_SA_STATE_COMPLETE, IKEEXT_QM_SA_STATE_FINAL, IKEEXT_QM_SA_STATE_INITIAL, IKEEXT_QM_SA_STATE_MAX, IKEEXT_QM_SA_STATE_NONE, fwp.ikeext_qm_sa_state, iketypes/IKEEXT_QM_SA_STATE, iketypes/IKEEXT_QM_SA_STATE_COMPLETE, iketypes/IKEEXT_QM_SA_STATE_FINAL, iketypes/IKEEXT_QM_SA_STATE_INITIAL, iketypes/IKEEXT_QM_SA_STATE_MAX, iketypes/IKEEXT_QM_SA_STATE_NONE
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
req.typenames: IKEEXT_QM_SA_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IKEEXT_QM_SA_STATE_
 - iketypes/IKEEXT_QM_SA_STATE_
 - IKEEXT_QM_SA_STATE
 - iketypes/IKEEXT_QM_SA_STATE
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
 - IKEEXT_QM_SA_STATE
---

# IKEEXT_QM_SA_STATE enumeration


## -description

The <b>IKEEXT_QM_SA_STATE</b> enumerated type defines the states for the Quick Mode (QM) negotiation exchanges that are part of the Authenticated Internet Protocol (AuthIP) and Internet Key Exchange (IKE) protocols.

## -enum-fields

### -field IKEEXT_QM_SA_STATE_NONE:0

Initial state.  No QM packets have been sent to the peer.

### -field IKEEXT_QM_SA_STATE_INITIAL

First packet has been sent to the peer.

### -field IKEEXT_QM_SA_STATE_FINAL

Final packet has been sent to the peer.

### -field IKEEXT_QM_SA_STATE_COMPLETE

QM has been completed.

### -field IKEEXT_QM_SA_STATE_MAX

Maximum value for testing purposes.

## -see-also

<a href="/windows/desktop/FWP/fwp-enums">Windows Filtering Platform API Enumerated Types</a>
