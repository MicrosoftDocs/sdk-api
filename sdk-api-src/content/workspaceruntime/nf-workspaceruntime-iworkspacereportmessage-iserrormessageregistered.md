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

# IWorkspaceReportMessage::IsErrorMessageRegistered


## -description


Determines whether a specified error message is registered in a specified workspace.


## -parameters




### -param bstrWkspId [in]

A string containing the ID of the workspace to check.


### -param dwErrorType [in]

The error type associated with the error message.


### -param bstrErrorMessageType [in]

A string containing the error message type.


### -param dwErrorCode [in]

The error code of the event.


### -param pfErrorExist [out, retval]

On success, returns a pointer to <b>VARIANT_TRUE</b> if the error message is registered in the specified workspace; otherwise, <b>VARIANT_FALSE</b>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/841fce89-2996-42eb-81fc-7d6f8f864398">IWorkspaceReportMessage</a>
 

 

