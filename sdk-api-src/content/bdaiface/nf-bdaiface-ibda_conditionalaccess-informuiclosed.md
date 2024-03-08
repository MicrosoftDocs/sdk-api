---
UID: NF:bdaiface.IBDA_ConditionalAccess.InformUIClosed
title: IBDA_ConditionalAccess::InformUIClosed (bdaiface.h)
description: The InformUIClosed method informs the device that the user-interface dialog is closed.
helpviewer_keywords: ["IBDA_ConditionalAccess interface [Microsoft TV Technologies]","InformUIClosed method","IBDA_ConditionalAccess.InformUIClosed","IBDA_ConditionalAccess::InformUIClosed","IBDA_ConditionalAccessInformUIClosed","InformUIClosed","InformUIClosed method [Microsoft TV Technologies]","InformUIClosed method [Microsoft TV Technologies]","IBDA_ConditionalAccess interface","bdaiface/IBDA_ConditionalAccess::InformUIClosed","mstv.ibda_conditionalaccess_informuiclosed"]
old-location: mstv\ibda_conditionalaccess_informuiclosed.htm
tech.root: mstv
ms.assetid: 8f9dcd29-ccd9-4154-bf11-932a3635c156
ms.date: 12/05/2018
ms.keywords: IBDA_ConditionalAccess interface [Microsoft TV Technologies],InformUIClosed method, IBDA_ConditionalAccess.InformUIClosed, IBDA_ConditionalAccess::InformUIClosed, IBDA_ConditionalAccessInformUIClosed, InformUIClosed, InformUIClosed method [Microsoft TV Technologies], InformUIClosed method [Microsoft TV Technologies],IBDA_ConditionalAccess interface, bdaiface/IBDA_ConditionalAccess::InformUIClosed, mstv.ibda_conditionalaccess_informuiclosed
req.header: bdaiface.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: None supported
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
 - IBDA_ConditionalAccess::InformUIClosed
 - bdaiface/IBDA_ConditionalAccess::InformUIClosed
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Bdaiface.h
api_name:
 - IBDA_ConditionalAccess.InformUIClosed
---

# IBDA_ConditionalAccess::InformUIClosed


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>InformUIClosed</b> method informs the device that the user-interface dialog is closed.

## -parameters

### -param byDialogNumber [in]

Specifies the dialog number.

### -param CloseReason [in]

Specifies the reason for closing the dialog, as a member of the <a href="/windows/desktop/api/bdaiface/ne-bdaiface-uiclosereasontype">UICloseReasonType</a> enumeration.

## -returns

If the method succeeds, it returns <b>S_OK</b>. It returns <b>S_FALSE</b> if a dialog with the specified dialog number cannot be found. If the method fails, it returns an error code.

## -see-also

<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_conditionalaccess">IBDA_ConditionalAccess Interface</a>