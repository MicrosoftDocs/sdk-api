---
UID: NF:bdaiface.IBDA_ConditionalAccessEx.OpenBroadcastMmi
title: IBDA_ConditionalAccessEx::OpenBroadcastMmi (bdaiface.h)
description: Responds to a BroadcastMMI event.
helpviewer_keywords: ["IBDA_ConditionalAccessEx interface [Microsoft TV Technologies]","OpenBroadcastMmi method","IBDA_ConditionalAccessEx.OpenBroadcastMmi","IBDA_ConditionalAccessEx::OpenBroadcastMmi","OpenBroadcastMmi","OpenBroadcastMmi method [Microsoft TV Technologies]","OpenBroadcastMmi method [Microsoft TV Technologies]","IBDA_ConditionalAccessEx interface","bdaiface/IBDA_ConditionalAccessEx::OpenBroadcastMmi","mstv.ibda_conditionalaccessex_openbroadcastmmi"]
old-location: mstv\ibda_conditionalaccessex_openbroadcastmmi.htm
tech.root: mstv
ms.assetid: 15390805-ff09-4dca-b00d-ad2f3641911b
ms.date: 12/05/2018
ms.keywords: IBDA_ConditionalAccessEx interface [Microsoft TV Technologies],OpenBroadcastMmi method, IBDA_ConditionalAccessEx.OpenBroadcastMmi, IBDA_ConditionalAccessEx::OpenBroadcastMmi, OpenBroadcastMmi, OpenBroadcastMmi method [Microsoft TV Technologies], OpenBroadcastMmi method [Microsoft TV Technologies],IBDA_ConditionalAccessEx interface, bdaiface/IBDA_ConditionalAccessEx::OpenBroadcastMmi, mstv.ibda_conditionalaccessex_openbroadcastmmi
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
 - IBDA_ConditionalAccessEx::OpenBroadcastMmi
 - bdaiface/IBDA_ConditionalAccessEx::OpenBroadcastMmi
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
 - IBDA_ConditionalAccessEx.OpenBroadcastMmi
---

# IBDA_ConditionalAccessEx::OpenBroadcastMmi


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Responds to a BroadcastMMI event.

When a device receives a BroadcastMMI event, it calls this method one time for each user interface (MMI) dialog box that is displayed to the user.

## -parameters

### -param ulDialogRequest [in]

A logical link with the MMI dialog box that was triggered by the action.

### -param bstrLanguage [in]

The language of the dialog box. This string contains an ISO 639-2 language code with a dash followed by an ISO 3166 country/region code.

### -param EventId [in]

The event identifier of the BroadcastMMI event.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_conditionalaccessex">IBDA_ConditionalAccessEx</a>