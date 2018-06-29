---
UID: NF:mi.MI_Session_Invoke
title: MI_Session_Invoke function
author: windows-sdk-content
description: Invokes a method in the provider.
old-location: wmi_v2\mi_session_invoke.htm
old-project: wmi_v2
ms.assetid: 46bce0cc-9795-47af-8318-4250dc3d5c6e
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: MI_Session_Invoke, MI_Session_Invoke function [Windows Management Infrastructure (MI)], mi/MI_Session_Invoke, wmi_v2.mi_session_invoke
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: MI_Type
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mi.h
api_name:
 - MI_Session_Invoke
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_Session_Invoke function


## -description


Invokes a method in the provider.


## -parameters




### -param session [in]

Session handle returned from 
    <a href="https://msdn.microsoft.com/76010766-aa20-4632-940d-48d9769803da">MI_Application_NewSession</a>.


### -param flags

Runtime type information (RTTI) 
      <a href="https://msdn.microsoft.com/library/JJ653875(v=VS.85).aspx">flags</a>.


### -param options [in, optional]

Optional <a href="https://msdn.microsoft.com/60445a53-c40c-4d0a-9650-21d0c7f3bbf6">MI_OperationOptions</a> value that 
      specifies options such as timeouts and how to control the CIM semantics. Specify <b>Null</b> 
      if no operation options are to be sent.


### -param namespaceName [in, optional]

An optional, null-terminated string that represents the namespace name to carry out the operation. If none 
      is specified, the server will pick a default.  The namespace cannot include a computer name.  It can only be in 
      the form of a namespace name separated by a slash mark character (/). For example, the following would be a 
      valid <b>namespaceName</b> value: <b>root/cimv2</b>.


### -param className [in, optional]

An optional, null-terminated string that represents the name of the class the method is a part of. Should 
      be <b>Null</b> when passing in an <b>inboundinstance</b>.


### -param methodName [in]

A null-terminated string that represents the name of the method to invoke.


### -param inboundInstance [in, optional]

Instance with keys to specify which method is to be invoked. If <b>Null</b>, the method 
      must be static.


### -param inboundProperties [in, optional]

Inbound method properties. Each inbound property needs to be an element in the instance and the element 
      name needs to be the same as the name of the method parameter.


### -param callbacks [in, optional]

Optional <a href="https://msdn.microsoft.com/f56954bf-c1aa-408b-bc45-0faf2a99b381">MI_OperationCallbacks</a> structure 
      that defines the operational callbacks to receive the instance result and CIM semantics. To carry out the 
      operation asynchronously, the structure's <b>instanceResult</b> callback member must be 
      specified. If this member is not specified, then the client must call the 
      <a href="https://msdn.microsoft.com/25c2d3fa-276d-4506-a044-4057c8cdc863">MI_Operation_GetInstance</a> function to 
      retrieve the results.


### -param operation [out]

Returned operation handle that must be closed via 
      <a href="https://msdn.microsoft.com/3e698e34-d537-4ea4-9345-cc4f493ff823">MI_Operation_Close</a> once complete.  Calling 
      <a href="https://msdn.microsoft.com/11a9f9f6-9dfa-4f7c-9562-f4793c007f04">MI_Operation_Cancel</a> before it is complete 
      will cause the operation to shutdown. 
      <b>MI_Operation_Close</b> and 
      <b>MI_Operation_Cancel</b> can be called from any 
      operation.


## -remarks



Methods have return values that will be returned as a <i>ReturnValue</i> parameter of the 
    outbound instance. There may be outbound properties that will be part of the same result. If the streamed 
    parameter callback is given and any outbound properties are marked as streamed, the streaming callback will be 
    called for each parameter that supports streaming. They will be called until all results are retrieved or until 
    the final result is given back.




## -see-also




<a href="https://msdn.microsoft.com/76010766-aa20-4632-940d-48d9769803da">MI_Application_NewSession</a>



<a href="https://msdn.microsoft.com/f56954bf-c1aa-408b-bc45-0faf2a99b381">MI_OperationCallbacks</a>



<a href="https://msdn.microsoft.com/11a9f9f6-9dfa-4f7c-9562-f4793c007f04">MI_Operation_Cancel</a>



<a href="https://msdn.microsoft.com/3e698e34-d537-4ea4-9345-cc4f493ff823">MI_Operation_Close</a>



<a href="https://msdn.microsoft.com/25c2d3fa-276d-4506-a044-4057c8cdc863">MI_Operation_GetInstance</a>
 

 

