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

# IBDA_ConditionalAccessEx::CloseMmiDialog


## -description


Notifies the Conditional Access Service (CAS) that the media sink device (MSD) has closed a user interface (MMI) dialog.


## -parameters




### -param ulDialogRequest [in]

A logical link with the user interface (MMI) dialog that was triggered by the action.


### -param bstrLanguage [in]

The language for any dialogs resulting from this action. This string contains an ISO 639-2 language code with a dash followed by an ISO 3166 country/region code.


### -param ulDialogNumber [in]

The dialog number of the dialog that was closed.


### -param ReasonCode [in]

The reason for closing the dialog,  specified as a member of the <a href="https://msdn.microsoft.com/d35067b3-a50b-4bc8-9139-429fe4fa25bb">BDA_CONDITIONALACCESS_MMICLOSEREASON</a> enumeration.


### -param pulSessionResult [out]

Receives the result code for the MMI session. For more information, see <i>Protected Broadcast Driver Architecture, Part 1: Core Services - CAS</i>, section 2.6.6. You can download this specification from <a href="http://go.microsoft.com/fwlink/p/?linkid=132926">http://go.microsoft.com/fwlink/p/?linkid=132926</a>. (This resource may not be available in some languages 

and countries.)


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/9db9b6b1-fc4f-48f0-940e-d79a321ef094">IBDA_ConditionalAccessEx</a>
 

 

