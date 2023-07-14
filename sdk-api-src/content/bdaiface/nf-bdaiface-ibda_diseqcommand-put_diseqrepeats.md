---
UID: NF:bdaiface.IBDA_DiseqCommand.put_DiseqRepeats
title: IBDA_DiseqCommand::put_DiseqRepeats (bdaiface.h)
description: Enables or disables repeated Digital Satellite Equipment Control (DiSEqC) commands.
helpviewer_keywords: ["IBDA_DiseqCommand interface [Microsoft TV Technologies]","put_DiseqRepeats method","IBDA_DiseqCommand.put_DiseqRepeats","IBDA_DiseqCommand::put_DiseqRepeats","bdaiface/IBDA_DiseqCommand::put_DiseqRepeats","mstv.ibda_diseqcommand_put_diseqrepeats","put_DiseqRepeats","put_DiseqRepeats method [Microsoft TV Technologies]","put_DiseqRepeats method [Microsoft TV Technologies]","IBDA_DiseqCommand interface"]
old-location: mstv\ibda_diseqcommand_put_diseqrepeats.htm
tech.root: mstv
ms.assetid: de5cbfa9-1509-47cf-b994-24b5dac76d8e
ms.date: 12/05/2018
ms.keywords: IBDA_DiseqCommand interface [Microsoft TV Technologies],put_DiseqRepeats method, IBDA_DiseqCommand.put_DiseqRepeats, IBDA_DiseqCommand::put_DiseqRepeats, bdaiface/IBDA_DiseqCommand::put_DiseqRepeats, mstv.ibda_diseqcommand_put_diseqrepeats, put_DiseqRepeats, put_DiseqRepeats method [Microsoft TV Technologies], put_DiseqRepeats method [Microsoft TV Technologies],IBDA_DiseqCommand interface
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
 - IBDA_DiseqCommand::put_DiseqRepeats
 - bdaiface/IBDA_DiseqCommand::put_DiseqRepeats
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
 - IBDA_DiseqCommand.put_DiseqRepeats
---

# IBDA_DiseqCommand::put_DiseqRepeats


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Enables or disables repeated Digital Satellite Equipment Control (DiSEqC) commands.

## -parameters

### -param ulRepeats [in]

The number of times to repeat each DiSEqC command. To disable repeated commands, set <i>ulRepeats</i> to 0.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

When two DiSEqC switches are cascaded, the tuner might have to repeat
commands for the far device. However, repeated commands can increase  the amount of time required for tuning by about 100 milliseconds. Therefore, it is recommended to disable repeated commands if they are not required.

## -see-also

<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_diseqcommand">IBDA_DiseqCommand</a>