---
UID: NS:mi._MI_OperationCallbacks
title: "_MI_OperationCallbacks"
author: windows-sdk-content
description: Structure that holds all callback function pointers for carrying out operations.
old-location: wmi_v2\mi_operationcallbacks.htm
tech.root: wmi_v2
ms.assetid: f56954bf-c1aa-408b-bc45-0faf2a99b381
ms.author: windowssdkdev
ms.date: 08/13/2018
ms.keywords: MI_OperationCallbacks, MI_OperationCallbacks structure [Windows Management Infrastructure (MI)], _MI_OperationCallbacks, mi/MI_OperationCallbacks, wmi._mi_operationcallbacks, wmi_v2.mi_operationcallbacks
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: mi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
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
 - HeaderDef
api_location:
 - Mi.h
api_name:
 - MI_OperationCallbacks
product: Windows
targetos: Windows
req.typenames: MI_OperationCallbacks
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
---

# _MI_OperationCallbacks structure


## -description


Structure that holds all callback function pointers for carrying out operations.


## -struct-fields




### -field callbackContext

A client specific context that is passed to all the callbacks. This is used to correlate the callback to the associated operation. This value will be passed to any operation callbacks.


### -field promptUser

Optional callback to handle prompt user requests from the server.


### -field writeError

Optional callback to receive write error messages from the server.


### -field writeMessage

Optional callback to receive write messages from the server.


### -field writeProgress

Optional callback to receive progress reports from the server.


### -field instanceResult

Optional instance callback to get asynchronous results from an operation.  If this is not specified and the operation is an instance operation, then the client will need to use the synchronous APIs to retrieve the results.


### -field indicationResult

Optional instance callback to get indication (subscribe) results from an operation.  If this is not specified and the operation is an instance operation, then the client will need to use the synchronous APIs to retrieve the results.


### -field classResult

Optional instance callback to get classes and class options from an operation.  If this is not specified and the operation is an instance operation, then the client will need to use the synchronous APIs to retrieve the results.


### -field streamedParameterResult

Optional callback to get streamed parameter results from method invocation operations.


## -remarks



All PowerShell Semantics and streamed result callbacks are optional;  include the callbacks 
 you want to receive. If the associated operation callback for the operation
is not set, i.e. set to <b>NULL</b>, the operation will be carried out synchronously. The client must call into the appropriate MI_Operation function to receive the results. The result callbacks will continue to be called until the moreResults field is equal to MI_FALSE.




## -see-also




<a href="https://msdn.microsoft.com/5CC9464F-1F50-405C-955E-F4CD18837CEC">MI_OperationCallback_Class</a>



<a href="https://msdn.microsoft.com/737532E8-498A-4256-AFC9-0E91183BD9F6">MI_OperationCallback_Indication</a>



<a href="https://msdn.microsoft.com/DE36AC5F-4F22-4E38-BB26-F1CAADDB014C">MI_OperationCallback_Instance</a>



<a href="https://msdn.microsoft.com/EF6DA690-B84F-40BA-A455-6AE745644057">MI_OperationCallback_PromptUser</a>



<a href="https://msdn.microsoft.com/BDD04E51-C168-4143-8A58-18402C7F12A0">MI_OperationCallback_StreamedParameter</a>



<a href="https://msdn.microsoft.com/B2BF45DD-4E6F-4691-B2DD-B941A636A89D">MI_OperationCallback_WriteError</a>



<a href="https://msdn.microsoft.com/2B769AAA-4FC8-4324-A0A9-DB24D41D957B">MI_OperationCallback_WriteMessage</a>



<a href="https://msdn.microsoft.com/B0AC5AB7-B635-4A95-AEBB-33B7AE633B40">MI_OperationCallback_WriteProgress</a>
 

 

