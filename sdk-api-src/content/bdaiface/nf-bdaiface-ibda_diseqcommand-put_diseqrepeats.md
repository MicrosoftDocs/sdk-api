---
UID: NF:bdaiface.IBDA_DiseqCommand.put_DiseqRepeats
title: IBDA_DiseqCommand::put_DiseqRepeats
author: windows-sdk-content
description: Enables or disables repeated Digital Satellite Equipment Control (DiSEqC) commands.
old-location: mstv\ibda_diseqcommand_put_diseqrepeats.htm
old-project: mstv
ms.assetid: de5cbfa9-1509-47cf-b994-24b5dac76d8e
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: IBDA_DiseqCommand interface [Microsoft TV Technologies],put_DiseqRepeats method, IBDA_DiseqCommand.put_DiseqRepeats, IBDA_DiseqCommand::put_DiseqRepeats, bdaiface/IBDA_DiseqCommand::put_DiseqRepeats, mstv.ibda_diseqcommand_put_diseqrepeats, put_DiseqRepeats, put_DiseqRepeats method [Microsoft TV Technologies], put_DiseqRepeats method [Microsoft TV Technologies],IBDA_DiseqCommand interface
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: UICloseReasonType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - bdaiface.h
api_name:
 - IBDA_DiseqCommand.put_DiseqRepeats
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IBDA_DiseqCommand::put_DiseqRepeats


## -description


Enables or disables repeated Digital Satellite Equipment Control (DiSEqC) commands.


## -parameters




### -param ulRepeats [in]

The number of times to repeat each DiSEqC command. To disable repeated commands, set <i>ulRepeats</i> to 0.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



When two DiSEqC switches are cascaded, the tuner might have to repeat
commands for the far device. However, repeated commands can increase  the amount of time required for tuning by about 100 milliseconds. Therefore, it is recommended to disable repeated commands if they are not required.




## -see-also




<a href="https://msdn.microsoft.com/0148a32d-b131-46ba-bbf0-82e2cf9c7d86">IBDA_DiseqCommand</a>
 

 

