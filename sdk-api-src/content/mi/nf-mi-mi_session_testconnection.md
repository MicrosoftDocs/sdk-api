---
UID: NF:mi.MI_Session_TestConnection
title: MI_Session_TestConnection function
author: windows-sdk-content
description: Tests a connection by communicating with the server represented by the session to determine whether it is responding.
old-location: wmi_v2\mi_session_testconnection.htm
old-project: wmi_v2
ms.assetid: 513eb39c-6894-49fa-bc4d-932f25318c34
ms.author: windowssdkdev
ms.date: 06/14/2018
ms.keywords: MI_Session_TestConnection, MI_Session_TestConnection function [Windows Management Infrastructure (MI)], mi/MI_Session_TestConnection, wmi_v2.mi_session_testconnection
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
 - MI_Session_TestConnection
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_Session_TestConnection function


## -description


Tests a connection by communicating with the server represented by the session to determine whether it is responding.


## -parameters




### -param session [in]

Session handle returned from <a href="https://msdn.microsoft.com/76010766-aa20-4632-940d-48d9769803da">MI_Application_NewSession</a>.


### -param flags

Must be 0.


### -param callbacks [in, optional]

Optional <a href="https://msdn.microsoft.com/f56954bf-c1aa-408b-bc45-0faf2a99b381">MI_OperationCallbacks</a> structure that defines the operational callbacks to receive the instance result and CIM semantics. To carry out the operation asynchronously, the structure's <b>instanceResult</b> callback member must be specified. If this member is not specified, the client must call the <a href="https://msdn.microsoft.com/25c2d3fa-276d-4506-a044-4057c8cdc863">MI_Operation_GetInstance</a> function to retrieve the results.


### -param operation [out]

Returned operation handle that must be closed via <a href="https://msdn.microsoft.com/3e698e34-d537-4ea4-9345-cc4f493ff823">MI_Operation_Close</a> once complete.  Calling <a href="https://msdn.microsoft.com/11a9f9f6-9dfa-4f7c-9562-f4793c007f04">MI_Operation_Cancel</a> before it is complete will cause the operation to shutdown.  <b>MI_Operation_Close</b> and <b>MI_Operation_Cancel</b> can be called from any operation.


## -see-also




<a href="https://msdn.microsoft.com/76010766-aa20-4632-940d-48d9769803da">MI_Application_NewSession</a>



<a href="https://msdn.microsoft.com/f56954bf-c1aa-408b-bc45-0faf2a99b381">MI_OperationCallbacks</a>



<a href="https://msdn.microsoft.com/11a9f9f6-9dfa-4f7c-9562-f4793c007f04">MI_Operation_Cancel</a>



<a href="https://msdn.microsoft.com/3e698e34-d537-4ea4-9345-cc4f493ff823">MI_Operation_Close</a>



<a href="https://msdn.microsoft.com/25c2d3fa-276d-4506-a044-4057c8cdc863">MI_Operation_GetInstance</a>
 

 

