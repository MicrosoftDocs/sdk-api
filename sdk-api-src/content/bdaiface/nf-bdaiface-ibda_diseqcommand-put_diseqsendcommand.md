---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IBDA_DiseqCommand::put_DiseqSendCommand


## -description


Sends a Digital Satellite Equipment Control (DiSEqC) command.


## -parameters




### -param ulRequestId [in]

An identifier for the command that is assigned by the application.


### -param ulcbCommandLen [in]

The size of the <i>pbCommand</i> array, in bytes.


### -param pbCommand [in]

Pointer to a byte array that contains the DiSEqC command, starting with the framing byte. The driver inserts the parity bits for the command.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is required for version 1.2 and later of the DiSEqC command set.

To get the command response from the driver, call <a href="https://msdn.microsoft.com/ed481bfb-dd80-44fa-bf64-a0f8e903ae35">IBDA_DiseqCommand::get_DiseqResponse</a>.




## -see-also




<a href="https://msdn.microsoft.com/0148a32d-b131-46ba-bbf0-82e2cf9c7d86">IBDA_DiseqCommand</a>
 

 

