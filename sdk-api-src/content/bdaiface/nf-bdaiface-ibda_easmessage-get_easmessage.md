---
UID: NF:bdaiface.IBDA_EasMessage.get_EasMessage
title: IBDA_EasMessage::get_EasMessage (bdaiface.h)
description: The get_EasMessage method retrieves an EAS message.
helpviewer_keywords: ["IBDA_EasMessage interface [Microsoft TV Technologies]","get_EasMessage method","IBDA_EasMessage.get_EasMessage","IBDA_EasMessage::get_EasMessage","IBDA_EasMessageget_EasMessage","bdaiface/IBDA_EasMessage::get_EasMessage","get_EasMessage","get_EasMessage method [Microsoft TV Technologies]","get_EasMessage method [Microsoft TV Technologies]","IBDA_EasMessage interface","mstv.ibda_easmessage_get_easmessage"]
old-location: mstv\ibda_easmessage_get_easmessage.htm
tech.root: mstv
ms.assetid: ac6454f2-28e6-4cb2-8b48-517d4dd8509c
ms.date: 12/05/2018
ms.keywords: IBDA_EasMessage interface [Microsoft TV Technologies],get_EasMessage method, IBDA_EasMessage.get_EasMessage, IBDA_EasMessage::get_EasMessage, IBDA_EasMessageget_EasMessage, bdaiface/IBDA_EasMessage::get_EasMessage, get_EasMessage, get_EasMessage method [Microsoft TV Technologies], get_EasMessage method [Microsoft TV Technologies],IBDA_EasMessage interface, mstv.ibda_easmessage_get_easmessage
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
 - IBDA_EasMessage::get_EasMessage
 - bdaiface/IBDA_EasMessage::get_EasMessage
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
 - IBDA_EasMessage.get_EasMessage
---

# IBDA_EasMessage::get_EasMessage


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_EasMessage</b> method retrieves an EAS message.

## -parameters

### -param ulEventID [in]

Specifies the event ID of the EAS message.

### -param ppEASObject [in, out]

Pointer to a pointer variable that receives a pointer to the <b>IUnknown</b> interface of the EAS object. The caller can query this object for its <a href="/previous-versions/windows/desktop/api/atscpsipparser/nn-atscpsipparser-iscte_eas">ISCTE_EAS</a> interface.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

This method retrieves a counted reference to an <b>IUnknown</b> interface instance. The caller is responsible for releasing the interface when it is no longer required.

## -see-also

<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_easmessage">IBDA_EasMessage Interface</a>