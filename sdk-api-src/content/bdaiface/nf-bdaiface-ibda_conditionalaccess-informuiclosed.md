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
 

 

