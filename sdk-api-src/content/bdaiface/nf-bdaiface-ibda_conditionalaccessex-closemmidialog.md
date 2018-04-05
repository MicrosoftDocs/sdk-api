---
UID: NF:bdaiface.IBDA_ConditionalAccessEx.CloseMmiDialog
title: IBDA_ConditionalAccessEx::CloseMmiDialog method
author: windows-driver-content
description: Notifies the Conditional Access Service (CAS) that the media sink device (MSD) has closed a user interface (MMI) dialog.
old-location: mstv\ibda_conditionalaccessex_closemmidialog.htm
old-project: mstv
ms.assetid: 30cba76b-ae52-4c87-a88e-faa9ad3f12f9
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: CloseMmiDialog method [Microsoft TV Technologies], CloseMmiDialog method [Microsoft TV Technologies], IBDA_ConditionalAccessEx interface, CloseMmiDialog,IBDA_ConditionalAccessEx.CloseMmiDialog, IBDA_ConditionalAccessEx, IBDA_ConditionalAccessEx interface [Microsoft TV Technologies], CloseMmiDialog method, IBDA_ConditionalAccessEx::CloseMmiDialog, bdaiface/IBDA_ConditionalAccessEx::CloseMmiDialog, mstv.ibda_conditionalaccessex_closemmidialog
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: UICloseReasonType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	bdaiface.h
api_name:
-	IBDA_ConditionalAccessEx.CloseMmiDialog
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IBDA_ConditionalAccessEx::CloseMmiDialog method


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
 

 

