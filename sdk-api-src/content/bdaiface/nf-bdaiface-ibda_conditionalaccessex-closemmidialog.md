---
UID: NF:bdaiface.IBDA_ConditionalAccessEx.CloseMmiDialog
title: IBDA_ConditionalAccessEx::CloseMmiDialog (bdaiface.h)
description: Notifies the Conditional Access Service (CAS) that the media sink device (MSD) has closed a user interface (MMI) dialog.
helpviewer_keywords: ["CloseMmiDialog","CloseMmiDialog method [Microsoft TV Technologies]","CloseMmiDialog method [Microsoft TV Technologies]","IBDA_ConditionalAccessEx interface","IBDA_ConditionalAccessEx interface [Microsoft TV Technologies]","CloseMmiDialog method","IBDA_ConditionalAccessEx.CloseMmiDialog","IBDA_ConditionalAccessEx::CloseMmiDialog","bdaiface/IBDA_ConditionalAccessEx::CloseMmiDialog","mstv.ibda_conditionalaccessex_closemmidialog"]
old-location: mstv\ibda_conditionalaccessex_closemmidialog.htm
tech.root: mstv
ms.assetid: 30cba76b-ae52-4c87-a88e-faa9ad3f12f9
ms.date: 12/05/2018
ms.keywords: CloseMmiDialog, CloseMmiDialog method [Microsoft TV Technologies], CloseMmiDialog method [Microsoft TV Technologies],IBDA_ConditionalAccessEx interface, IBDA_ConditionalAccessEx interface [Microsoft TV Technologies],CloseMmiDialog method, IBDA_ConditionalAccessEx.CloseMmiDialog, IBDA_ConditionalAccessEx::CloseMmiDialog, bdaiface/IBDA_ConditionalAccessEx::CloseMmiDialog, mstv.ibda_conditionalaccessex_closemmidialog
req.header: bdaiface.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bdaiface.idl
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
 - IBDA_ConditionalAccessEx::CloseMmiDialog
 - bdaiface/IBDA_ConditionalAccessEx::CloseMmiDialog
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - bdaiface.h
api_name:
 - IBDA_ConditionalAccessEx.CloseMmiDialog
---

# IBDA_ConditionalAccessEx::CloseMmiDialog


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Notifies the Conditional Access Service (CAS) that the media sink device (MSD) has closed a user interface (MMI) dialog.

## -parameters

### -param ulDialogRequest [in]

A logical link with the user interface (MMI) dialog that was triggered by the action.

### -param bstrLanguage [in]

The language for any dialogs resulting from this action. This string contains an ISO 639-2 language code with a dash followed by an ISO 3166 country/region code.

### -param ulDialogNumber [in]

The dialog number of the dialog that was closed.

### -param ReasonCode [in]

The reason for closing the dialog,  specified as a member of the <a href="/previous-versions/windows/desktop/mstv/bda-conditionalaccess-mmiclosereason">BDA_CONDITIONALACCESS_MMICLOSEREASON</a> enumeration.

### -param pulSessionResult [out]

Receives the result code for the MMI session. For more information, see <i>Protected Broadcast Driver Architecture, Part 1: Core Services - CAS</i>, section 2.6.6.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_conditionalaccessex">IBDA_ConditionalAccessEx</a>