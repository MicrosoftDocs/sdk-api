---
UID: NS:resapi.CLRES_CALLBACK_FUNCTION_TABLE
title: CLRES_CALLBACK_FUNCTION_TABLE
author: windows-sdk-content
description: Represents a function table for the StartupEx callback function.
old-location: mscs\clres_callback_function_table.htm
old-project: mscs
ms.assetid: 1B67B70B-330D-4BA5-AA6C-408588868C76
ms.author: windowssdkdev
ms.date: 07/12/2018
ms.keywords: "*PCLRES_CALLBACK_FUNCTION_TABLE, CLRES_CALLBACK_FUNCTION_TABLE, CLRES_CALLBACK_FUNCTION_TABLE structure [Failover Cluster], PCLRES_CALLBACK_FUNCTION_TABLE, PCLRES_CALLBACK_FUNCTION_TABLE structure pointer [Failover Cluster], mscs.clres_callback_function_table, resapi/CLRES_CALLBACK_FUNCTION_TABLE, resapi/PCLRES_CALLBACK_FUNCTION_TABLE"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: resapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.typenames: CLRES_CALLBACK_FUNCTION_TABLE, *PCLRES_CALLBACK_FUNCTION_TABLE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ResApi.h
api_name:
 - CLRES_CALLBACK_FUNCTION_TABLE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# CLRES_CALLBACK_FUNCTION_TABLE structure


## -description


Represents a function table for the <a href="https://msdn.microsoft.com/7C669EDC-B7A1-4623-91A9-5D8C5949B50A">StartupEx</a> callback function.


## -struct-fields




### -field LogEvent

A pointer to the <a href="https://msdn.microsoft.com/91389083-e007-4d64-885f-e5188e74b9d8">LogEvent</a> entry point.


### -field SetResourceStatusEx

A pointer to the <a href="https://msdn.microsoft.com/3733F912-9D43-489B-91D8-7128D0F5D1A4">SetResourceStatusEx</a> entry point.


### -field SetResourceLockedMode

A pointer to the <a href="https://msdn.microsoft.com/000D127C-7BDE-4FC1-984E-2EE805E603FC">SetResourceLockedMode</a> entry point.


### -field SignalFailure

A pointer to the <a href="https://msdn.microsoft.com/C4226174-B983-4BF5-8DA5-638201124037">SignalFailure</a> entry point.


### -field SetResourceInMemoryNodeLocalProperties

A pointer to the <a href="https://msdn.microsoft.com/9263E130-49DE-465C-A852-34E2D93A4211">SetResourceInMemoryNodeLocalProperties</a> entry point.


### -field EndControlCall

A pointer to the <a href="https://msdn.microsoft.com/0FB2C129-B98C-4570-8621-6BAD46911682">EndControlCall</a> entry point.

<b>Windows Server 2012:  </b>This member was added in Windows Server 2012 R2.


### -field EndTypeControlCall

A pointer to the <a href="https://msdn.microsoft.com/EF3C2DFA-2B8A-4709-A6B6-56427C0C00A5">EndTypeControlCall</a> entry point.

<b>Windows Server 2012:  </b>This member was added in Windows Server 2012 R2.


### -field ExtendControlCall

A pointer to the <a href="https://msdn.microsoft.com/79607FE9-96E5-4854-BC92-8FF1C474B3D6">ExtendControlCall</a> entry point.

<b>Windows Server 2012 R2 and Windows Server 2012:  </b>This member was added in Windows Server 2016.


### -field ExtendTypeControlCall

A pointer to the <a href="https://msdn.microsoft.com/90E9A989-D281-440D-8441-02086841356E">ExtendResTypeControlCall</a> entry point.

<b>Windows Server 2012 R2 and Windows Server 2012:  </b>This member was added in Windows Server 2016.


### -field RaiseResTypeNotification

A pointer to the <a href="https://msdn.microsoft.com/9F5C8008-6B7B-4CA9-896C-15E5A3FB68C9">RaiseResTypeNotification</a> entry point.

<b>Windows Server 2012 R2 and Windows Server 2012:  </b>This member was added in Windows Server 2016.


### -field ChangeResourceProcessForDumps

A pointer to the <a href="https://msdn.microsoft.com/A404752F-4758-4133-8AD3-3137A4CA77D5">ChangeResourceProcessForDumps</a> entry point.

<b>Windows Server 2012 R2 and Windows Server 2012:  </b>This member was added in Windows Server 2016.


### -field ChangeResTypeProcessForDumps

A pointer to the <a href="https://msdn.microsoft.com/6E5CA26D-F58A-41A4-9ED0-35FA363B7025">ChangeResTypeProcessForDumps</a> entry point.

<b>Windows Server 2012 R2 and Windows Server 2012:  </b>This member was added in Windows Server 2016.


### -field SetInternalState

A pointer to the <a href="https://msdn.microsoft.com/B9ECD98B-D867-44C0-846F-8FE96E44F387">SetInternalState</a> entry point.

<b>Windows Server 2012 R2 and Windows Server 2012:  </b>This member was added in Windows Server 2016.


### -field SetResourceLockedModeEx

 




## -see-also




<a href="https://msdn.microsoft.com/9ab4b974-28b5-4f33-a7c4-b9b2472059aa">Resource DLL Structures</a>
 

 

