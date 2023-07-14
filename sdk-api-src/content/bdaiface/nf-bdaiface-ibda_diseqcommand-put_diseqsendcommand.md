---
UID: NF:bdaiface.IBDA_DiseqCommand.put_DiseqSendCommand
title: IBDA_DiseqCommand::put_DiseqSendCommand (bdaiface.h)
description: Sends a Digital Satellite Equipment Control (DiSEqC) command.
helpviewer_keywords: ["IBDA_DiseqCommand interface [Microsoft TV Technologies]","put_DiseqSendCommand method","IBDA_DiseqCommand.put_DiseqSendCommand","IBDA_DiseqCommand::put_DiseqSendCommand","bdaiface/IBDA_DiseqCommand::put_DiseqSendCommand","mstv.ibda_diseqcommand_put_diseqsendcommand","put_DiseqSendCommand","put_DiseqSendCommand method [Microsoft TV Technologies]","put_DiseqSendCommand method [Microsoft TV Technologies]","IBDA_DiseqCommand interface"]
old-location: mstv\ibda_diseqcommand_put_diseqsendcommand.htm
tech.root: mstv
ms.assetid: 5ee77311-0b1d-43b1-af8e-bb886170701d
ms.date: 12/05/2018
ms.keywords: IBDA_DiseqCommand interface [Microsoft TV Technologies],put_DiseqSendCommand method, IBDA_DiseqCommand.put_DiseqSendCommand, IBDA_DiseqCommand::put_DiseqSendCommand, bdaiface/IBDA_DiseqCommand::put_DiseqSendCommand, mstv.ibda_diseqcommand_put_diseqsendcommand, put_DiseqSendCommand, put_DiseqSendCommand method [Microsoft TV Technologies], put_DiseqSendCommand method [Microsoft TV Technologies],IBDA_DiseqCommand interface
req.header: bdaiface.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - IBDA_DiseqCommand::put_DiseqSendCommand
 - bdaiface/IBDA_DiseqCommand::put_DiseqSendCommand
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
 - IBDA_DiseqCommand.put_DiseqSendCommand
---

# IBDA_DiseqCommand::put_DiseqSendCommand


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Sends a Digital Satellite Equipment Control (DiSEqC) command.

## -parameters

### -param ulRequestId [in]

An identifier for the command that is assigned by the application.

### -param ulcbCommandLen [in]

The size of the <i>pbCommand</i> array, in bytes.

### -param pbCommand [in]

Pointer to a byte array that contains the DiSEqC command, starting with the framing byte. The driver inserts the parity bits for the command.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method is required for version 1.2 and later of the DiSEqC command set.

To get the command response from the driver, call <a href="/windows/desktop/api/bdaiface/nf-bdaiface-ibda_diseqcommand-get_diseqresponse">IBDA_DiseqCommand::get_DiseqResponse</a>.

## -see-also

<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_diseqcommand">IBDA_DiseqCommand</a>