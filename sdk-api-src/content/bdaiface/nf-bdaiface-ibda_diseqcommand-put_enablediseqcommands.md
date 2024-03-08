---
UID: NF:bdaiface.IBDA_DiseqCommand.put_EnableDiseqCommands
title: IBDA_DiseqCommand::put_EnableDiseqCommands (bdaiface.h)
description: Enables or disables the use of Digital Satellite Equipment Control (DiSEqC) commands.
helpviewer_keywords: ["IBDA_DiseqCommand interface [Microsoft TV Technologies]","put_EnableDiseqCommands method","IBDA_DiseqCommand.put_EnableDiseqCommands","IBDA_DiseqCommand::put_EnableDiseqCommands","bdaiface/IBDA_DiseqCommand::put_EnableDiseqCommands","mstv.ibda_diseqcommand_put_enablediseqcommands","put_EnableDiseqCommands","put_EnableDiseqCommands method [Microsoft TV Technologies]","put_EnableDiseqCommands method [Microsoft TV Technologies]","IBDA_DiseqCommand interface"]
old-location: mstv\ibda_diseqcommand_put_enablediseqcommands.htm
tech.root: mstv
ms.assetid: d70f5e3c-bd5d-48cf-b4fd-e1ae2ba66f69
ms.date: 12/05/2018
ms.keywords: IBDA_DiseqCommand interface [Microsoft TV Technologies],put_EnableDiseqCommands method, IBDA_DiseqCommand.put_EnableDiseqCommands, IBDA_DiseqCommand::put_EnableDiseqCommands, bdaiface/IBDA_DiseqCommand::put_EnableDiseqCommands, mstv.ibda_diseqcommand_put_enablediseqcommands, put_EnableDiseqCommands, put_EnableDiseqCommands method [Microsoft TV Technologies], put_EnableDiseqCommands method [Microsoft TV Technologies],IBDA_DiseqCommand interface
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
 - IBDA_DiseqCommand::put_EnableDiseqCommands
 - bdaiface/IBDA_DiseqCommand::put_EnableDiseqCommands
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
 - IBDA_DiseqCommand.put_EnableDiseqCommands
---

# IBDA_DiseqCommand::put_EnableDiseqCommands


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Enables or disables the use of Digital Satellite Equipment Control (DiSEqC) commands.

## -parameters

### -param bEnable [in]

If <b>TRUE</b>, DiSEqC commands are enabled. Otherwise, DiSEqC commands are disabled.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Depending on the satellite installation, DiSEqC commands might be required. However, enabling DiSEqC can result in the driver taking longer to switch transponders (typically by 100–300 milliseconds). Therefore, it is recommended to disable DiSEqC commands if they are not required.

## -see-also

<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_diseqcommand">IBDA_DiseqCommand</a>