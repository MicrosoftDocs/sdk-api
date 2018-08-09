---
UID: NF:bdaiface.IBDA_DiseqCommand.put_DiseqUseToneBurst
title: IBDA_DiseqCommand::put_DiseqUseToneBurst
author: windows-sdk-content
description: Enables or disables Tone-Burst commands.
old-location: mstv\ibda_diseqcommand_put_disequsetoneburst.htm
old-project: mstv
ms.assetid: 23523ac9-19e0-4247-a697-24d6f1c07285
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IBDA_DiseqCommand interface [Microsoft TV Technologies],put_DiseqUseToneBurst method, IBDA_DiseqCommand.put_DiseqUseToneBurst, IBDA_DiseqCommand::put_DiseqUseToneBurst, bdaiface/IBDA_DiseqCommand::put_DiseqUseToneBurst, mstv.ibda_diseqcommand_put_disequsetoneburst, put_DiseqUseToneBurst, put_DiseqUseToneBurst method [Microsoft TV Technologies], put_DiseqUseToneBurst method [Microsoft TV Technologies],IBDA_DiseqCommand interface
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
 - IBDA_DiseqCommand.put_DiseqUseToneBurst
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IBDA_DiseqCommand::put_DiseqUseToneBurst


## -description


Enables or disables Tone-Burst commands.


## -parameters




### -param bUseToneBurst [in]

If <b>TRUE</b>, Tone-Burst commands are enabled. Otherwise, Tone-Burst commands are disabled.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The Tone-Burst command uses a 22-kHz carrier signal to select either source position A or source position B. 

Typically the driver enables or disables Tone-Burst as needed when the application calls <a href="https://msdn.microsoft.com/09ed3d1d-026a-43b3-863b-a77260e082d8">IBDA_DiseqCommand::put_DiseqLNBSource</a>. However, you can use  the <b>put_DiseqUseToneBurst</b> method to switch this mode on or off, either to improve channel switching or to maintain compatibility with particular equipment. Note that using Tone-Burst can increase  the amount of time required for tuning by about 40 milliseconds.




## -see-also




<a href="https://msdn.microsoft.com/0148a32d-b131-46ba-bbf0-82e2cf9c7d86">IBDA_DiseqCommand</a>
 

 

