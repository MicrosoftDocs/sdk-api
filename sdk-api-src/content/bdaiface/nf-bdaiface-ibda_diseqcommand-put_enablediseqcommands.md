---
UID: NF:bdaiface.IBDA_DiseqCommand.put_EnableDiseqCommands
title: IBDA_DiseqCommand::put_EnableDiseqCommands
author: windows-driver-content
description: Enables or disables the use of Digital Satellite Equipment Control (DiSEqC) commands.
old-location: mstv\ibda_diseqcommand_put_enablediseqcommands.htm
old-project: mstv
ms.assetid: d70f5e3c-bd5d-48cf-b4fd-e1ae2ba66f69
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: IBDA_DiseqCommand interface [Microsoft TV Technologies],put_EnableDiseqCommands method, IBDA_DiseqCommand.put_EnableDiseqCommands, IBDA_DiseqCommand::put_EnableDiseqCommands, bdaiface/IBDA_DiseqCommand::put_EnableDiseqCommands, mstv.ibda_diseqcommand_put_enablediseqcommands, put_EnableDiseqCommands, put_EnableDiseqCommands method [Microsoft TV Technologies], put_EnableDiseqCommands method [Microsoft TV Technologies],IBDA_DiseqCommand interface
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: UICloseReasonType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	bdaiface.h
api_name:
-	IBDA_DiseqCommand.put_EnableDiseqCommands
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IBDA_DiseqCommand::put_EnableDiseqCommands


## -description


Enables or disables the use of Digital Satellite Equipment Control (DiSEqC) commands.


## -parameters




### -param bEnable [in]

If <b>TRUE</b>, DiSEqC commands are enabled. Otherwise, DiSEqC commands are disabled.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Depending on the satellite installation, DiSEqC commands might be required. However, enabling DiSEqC can result in the driver taking longer to switch transponders (typically by 100–300 milliseconds). Therefore, it is recommended to disable DiSEqC commands if they are not required. 




## -see-also




<a href="https://msdn.microsoft.com/0148a32d-b131-46ba-bbf0-82e2cf9c7d86">IBDA_DiseqCommand</a>
 

 

