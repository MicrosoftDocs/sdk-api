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

# IBDA_ISDBConditionalAccess::SetIsdbCasRequest


## -description


Sends a conditional access system (CAS) command for Integrated Services Digital Broadcasting (ISDB).


## -parameters




### -param ulRequestId [in]

The numeric code for the CAS command. The ARIB standard defines these values. Enumeration constants for some commands are defined in the <a href="https://msdn.microsoft.com/5c8a97bb-9d8b-4f4f-aeab-e8bf199a652e">ISDBCAS_REQUEST_ID</a> enumeration.


### -param ulcbRequestBufferLen [in]

Size of the <i>pbRequestBuffer</i> array, in bytes.


### -param pbRequestBuffer [in]

Pointer to a byte array that contains the data for the command.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/0e45e5ea-9f38-4a96-be44-8ee123492aa9">IBDA_ISDBConditionalAccess</a>
 

 

