---
UID: NF:mi.MI_Session_CreateInstance
title: MI_Session_CreateInstance function (mi.h)
author: windows-sdk-content
description: Creates an instance on the server that the session represents.
old-location: wmi_v2\mi_session_createinstance.htm
tech.root: wmi_v2
ms.assetid: ad4df737-4438-4bcd-8b58-ae5c6b25e95f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MI_Session_CreateInstance, MI_Session_CreateInstance function [Windows Management Infrastructure (MI)], mi/MI_Session_CreateInstance, wmi_v2.mi_session_createinstance
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
 - MI_Session_CreateInstance
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
---

# MI_Session_CreateInstance function


## -description


Creates an instance on the server that the session represents.


## -parameters




### -param session [in]

Session handle returned from <a href="https://msdn.microsoft.com/76010766-aa20-4632-940d-48d9769803da">MI_Application_NewSession</a>.


### -param flags

Runtime type information (RTTI) <a href="https://msdn.microsoft.com/24E82AC6-A2E3-4EC6-931F-26AC54D5CAA7">flags</a>.


### -param options [in, optional]

Optional <a href="https://msdn.microsoft.com/60445a53-c40c-4d0a-9650-21d0c7f3bbf6">MI_OperationOptions</a> value that specifies options such as timeouts and how to control the CIM semantics. Specify <b>Null</b> if no operation options are to be sent.


### -param namespaceName

A null-terminated string that contains the optional namespace name to carry out the operation.  If none is specified, the server will pick a default.  The namespace cannot include a computer name.  It can only be in the form of a namespace name separated by a slash mark character (/). For example, the following would be a valid <b>namespaceName</b> value: <b>root/cimv2</b>.


### -param inboundInstance [in]


<a href="https://msdn.microsoft.com/3dce1817-7995-49e5-8cc0-ee9496665e5c">MI_Instance</a> that represents the class name and keys of the instance to be created on the server along with the rest of the properties of the instance that destination instance will be set to.  Sometimes keys are read-only, so not all keys need to be specified. If the instance that is specified already exists, the function will fail; to update an existing instance, use the <a href="https://msdn.microsoft.com/4a01ac01-5d47-47ff-a331-6009a5c57204">MI_Session_ModifyInstance</a> function.


### -param callbacks [in, optional]

Optional <a href="https://msdn.microsoft.com/f56954bf-c1aa-408b-bc45-0faf2a99b381">MI_OperationCallbacks</a> structure that defines the operational callbacks to receive the instance result and CIM semantics. To do asynchronously, this value must be specified. If NULL is specified, the client must call the <a href="https://msdn.microsoft.com/25c2d3fa-276d-4506-a044-4057c8cdc863">MI_Operation_GetInstance</a> function to retrieve the results.


### -param operation [out]

Operation handle that must be closed with a call to <a href="https://msdn.microsoft.com/3e698e34-d537-4ea4-9345-cc4f493ff823">MI_Operation_Close</a> once the operation is finished and all results have been received. The handle can be used to cancel the operation with a call to <a href="https://msdn.microsoft.com/11a9f9f6-9dfa-4f7c-9562-f4793c007f04">MI_Operation_Cancel</a>.


## -see-also




<a href="https://msdn.microsoft.com/11a9f9f6-9dfa-4f7c-9562-f4793c007f04">MI_Operation_Cancel</a>



<a href="https://msdn.microsoft.com/3e698e34-d537-4ea4-9345-cc4f493ff823">MI_Operation_Close</a>



<a href="https://msdn.microsoft.com/25c2d3fa-276d-4506-a044-4057c8cdc863">MI_Operation_GetInstance</a>



<a href="https://msdn.microsoft.com/4a01ac01-5d47-47ff-a331-6009a5c57204">MI_Session_ModifyInstance</a>
 

 

