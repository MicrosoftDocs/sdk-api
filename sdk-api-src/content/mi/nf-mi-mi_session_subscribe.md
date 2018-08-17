---
UID: NF:mi.MI_Session_Subscribe
title: MI_Session_Subscribe function
author: windows-sdk-content
description: Subscribes to an indication on the server represented by the session.
old-location: wmi_v2\mi_session_subscribe.htm
old-project: wmi_v2
ms.assetid: fed64a7a-ef16-4e9b-91b4-7ecede099585
ms.author: windowssdkdev
ms.date: 08/13/2018
ms.keywords: MI_Session_Subscribe, MI_Session_Subscribe function [Windows Management Infrastructure (MI)], mi/MI_Session_Subscribe, wmi_v2.mi_session_subscribe
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: mi.h
req.include-header: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
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
 - MI_Session_Subscribe
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_Session_Subscribe function


## -description


Subscribes to an indication on the server represented by the session.


## -parameters




### -param session [in]

Session handle returned from <a href="https://msdn.microsoft.com/76010766-aa20-4632-940d-48d9769803da">MI_Application_NewSession</a>.


### -param flags

Runtime type information (RTTI) <a href="https://msdn.microsoft.com/24E82AC6-A2E3-4EC6-931F-26AC54D5CAA7">flags</a>.


### -param options [in, optional]

Optional <a href="https://msdn.microsoft.com/60445a53-c40c-4d0a-9650-21d0c7f3bbf6">MI_OperationOptions</a> value that specifies options such as timeouts and how to control the CIM semantics. Specify <b>Null</b> if no operation options are to be sent.


### -param namespaceName

An optional, null-terminated string that represents the namespace name to carry out the operation.  If none is specified, the server will pick a default.  The namespace cannot include a computer name.  It can only be in the form of a namespace name separated by a slash mark character (/). For example, the following would be a valid <b>namespaceName</b> value: <b>root/cimv2</b>.


### -param queryDialect

An optional, null-terminated string that represents the dialect of the query being passed. This value can be either WQL or CQL. Note that some servers do not support both dialects.


### -param queryExpression

An optional, null-terminated string that represents the query expression to be carried out.  Usually a query is needed, but if a WS-Management endpoint is being used, a resource URI can be passed. For WMI DCOM transport, this value must be specified.


### -param deliverOptions [in, optional]

Optional <a href="https://msdn.microsoft.com/aaed635c-ee53-4307-a5b4-e9d3bd2e7c21">MI_SubscriptionDeliveryOptions</a> structure that defines the subscription delivery options. For WMI DCOM transport, this value can be <b>Null</b>. For WinRM, this specifies settings such as delivery mode and push delivery credentials.


### -param callbacks [in, optional]

Optional <a href="https://msdn.microsoft.com/f56954bf-c1aa-408b-bc45-0faf2a99b381">MI_OperationCallbacks</a> structure that defines the operational callbacks to receive the instance result and CIM semantics. To carry out the operation asynchronously, the structure's <b>indicationResult</b> callback member must be specified. If this member is not specified, the client must call the <a href="https://msdn.microsoft.com/3e3e8472-ea33-485b-9e86-b5ba770af95b">MI_Operation_GetIndication</a> function to retrieve the results.


### -param operation [out]

Returned operation handle that must be closed via <a href="https://msdn.microsoft.com/3e698e34-d537-4ea4-9345-cc4f493ff823">MI_Operation_Close</a> once complete.  Calling <a href="https://msdn.microsoft.com/11a9f9f6-9dfa-4f7c-9562-f4793c007f04">MI_Operation_Cancel</a> before it is complete will cause the operation to shutdown.  <b>MI_Operation_Close</b> and <b>MI_Operation_Cancel</b> can be called from any operation.


## -remarks



You must have Audit privileges to use this function if specifying the push subscriptions option.




## -see-also




<a href="https://msdn.microsoft.com/76010766-aa20-4632-940d-48d9769803da">MI_Application_NewSession</a>



<a href="https://msdn.microsoft.com/f56954bf-c1aa-408b-bc45-0faf2a99b381">MI_OperationCallbacks</a>



<a href="https://msdn.microsoft.com/11a9f9f6-9dfa-4f7c-9562-f4793c007f04">MI_Operation_Cancel</a>



<a href="https://msdn.microsoft.com/3e698e34-d537-4ea4-9345-cc4f493ff823">MI_Operation_Close</a>



<a href="https://msdn.microsoft.com/3e3e8472-ea33-485b-9e86-b5ba770af95b">MI_Operation_GetIndication</a>



<a href="https://msdn.microsoft.com/6429e748-e0bf-431a-8989-db5b211665d5">Windows Remote Management</a>
 

 

