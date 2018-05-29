---
UID: NF:bdaiface.IBDA_ConditionalAccess.InformUIClosed
title: IBDA_ConditionalAccess::InformUIClosed
author: windows-sdk-content
description: The InformUIClosed method informs the device that the user-interface dialog is closed.
old-location: mstv\ibda_conditionalaccess_informuiclosed.htm
old-project: mstv
ms.assetid: 8f9dcd29-ccd9-4154-bf11-932a3635c156
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IBDA_ConditionalAccess interface [Microsoft TV Technologies],InformUIClosed method, IBDA_ConditionalAccess.InformUIClosed, IBDA_ConditionalAccess::InformUIClosed, IBDA_ConditionalAccessInformUIClosed, InformUIClosed, InformUIClosed method [Microsoft TV Technologies], InformUIClosed method [Microsoft TV Technologies],IBDA_ConditionalAccess interface, bdaiface/IBDA_ConditionalAccess::InformUIClosed, mstv.ibda_conditionalaccess_informuiclosed
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
req.typenames: UICloseReasonType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Bdaiface.h
api_name:
-	IBDA_ConditionalAccess.InformUIClosed
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IBDA_ConditionalAccess::InformUIClosed


## -description


The <b>InformUIClosed</b> method informs the device that the user-interface dialog is closed.


## -parameters




### -param byDialogNumber [in]

Specifies the dialog number.


### -param CloseReason [in]


            Specifies the reason for closing the dialog, as a member of the <a href="https://msdn.microsoft.com/ed609bf8-9675-40bc-a789-c98cbc96e45f">UICloseReasonType</a> enumeration.
          


## -returns



If the method succeeds, it returns <b>S_OK</b>. It returns <b>S_FALSE</b> if a dialog with the specified dialog number cannot be found. If the method fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/93bd3c38-2591-4d36-b296-5ad939487277">IBDA_ConditionalAccess Interface</a>
 

 

