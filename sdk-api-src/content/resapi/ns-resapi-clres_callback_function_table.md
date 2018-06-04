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
 

 

