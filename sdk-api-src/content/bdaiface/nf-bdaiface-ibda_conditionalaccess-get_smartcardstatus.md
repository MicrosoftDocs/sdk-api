---
UID: NF:bdaiface.IBDA_ConditionalAccess.get_SmartCardStatus
title: IBDA_ConditionalAccess::get_SmartCardStatus
author: windows-sdk-content
description: The get_SmartCardStatus method retrieves the status of the smart card.
old-location: mstv\ibda_conditionalaccess_get_smartcardstatus.htm
tech.root: MSTV
ms.assetid: 940247b0-c002-414f-9d01-9f4acfe90a35
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IBDA_ConditionalAccess interface [Microsoft TV Technologies],get_SmartCardStatus method, IBDA_ConditionalAccess.get_SmartCardStatus, IBDA_ConditionalAccess::get_SmartCardStatus, IBDA_ConditionalAccessget_SmartCardStatus, bdaiface/IBDA_ConditionalAccess::get_SmartCardStatus, get_SmartCardStatus, get_SmartCardStatus method [Microsoft TV Technologies], get_SmartCardStatus method [Microsoft TV Technologies],IBDA_ConditionalAccess interface, mstv.ibda_conditionalaccess_get_smartcardstatus
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Bdaiface.h
api_name:
 - IBDA_ConditionalAccess.get_SmartCardStatus
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBDA_ConditionalAccess::get_SmartCardStatus


## -description


The <b>get_SmartCardStatus</b> method retrieves the status of the smart card.


## -parameters




### -param pCardStatus [out]

Pointer to a variable of type <a href="https://msdn.microsoft.com/en-us/library/Dd695293(v=VS.85).aspx">SmartCardStatusType</a> that receives the card status type.
          


### -param pCardAssociation [out]

Pointer to a variable of type <a href="https://msdn.microsoft.com/en-us/library/Dd695292(v=VS.85).aspx">SmartCardAssociationType</a> that receives the card association type.
          


### -param pbstrCardError [out]

Receives a string containing the card error. When the string is no longer required, call the <b>SysFreeString</b> function to free it.
          


### -param pfOOBLocked

TBD




## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.
          




## -remarks



All three parameters must be non-NULL or the method fails and returns <b>E_POINTER</b>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd693261(v=VS.85).aspx">IBDA_ConditionalAccess Interface</a>
 

 

