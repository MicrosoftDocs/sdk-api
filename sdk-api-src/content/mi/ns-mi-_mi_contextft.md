---
UID: NS:mi._MI_ContextFT
title: "_MI_ContextFT"
author: windows-sdk-content
description: A support structure used in the MI_Context structure. Use the functions with the name prefix &#0034;MI_Context_&#0034; to manipulate these structures.
old-location: wmi_v2\mi_contextft.htm
old-project: wmi_v2
ms.assetid: a5a3003f-9343-415d-b30f-32b479232db8
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: MI_ContextFT, MI_ContextFT structure [Windows Management Infrastructure (MI)], _MI_ContextFT, mi/MI_ContextFT, wmi_v2.mi_contextft
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
tech.root: 
req.typenames: MI_ContextFT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mi.h
api_name:
 - MI_ContextFT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _MI_ContextFT structure


## -description


A support structure used in the <a href="https://msdn.microsoft.com/51d6c510-f9fd-4ab7-a669-b2a5776b496d">MI_Context</a> 
     structure. Use the functions with the name prefix "MI_Context_" to manipulate these 
     structures.


## -struct-fields






#### - Canceled

Determines whether the operation has been canceled. See 
       <a href="https://msdn.microsoft.com/d8050079-978d-461b-8cf7-e6a08e4d026f">MI_Context_Canceled</a>.


#### - ConstructInstance

Initializes an instance. See 
       <a href="https://msdn.microsoft.com/c1b90938-401a-4fae-99de-9954d02b892e">MI_Context_ConstructInstance</a>.


#### - ConstructParameters

Initialize a parameters instance. See 
       <a href="https://msdn.microsoft.com/dd5bea1c-fee0-4ebf-9c4c-a42bf9ba315b">MI_Context_ConstructParameters</a>.


#### - GetCustomOption

Gets the specified provider custom option. See 
       <a href="https://msdn.microsoft.com/3338ca5c-48ac-450f-bf2a-ded6a2c3da19">MI_Context_GetCustomOption</a>.


#### - GetCustomOptionAt

Gets the provider's custom option at the specified index. See 
       <a href="https://msdn.microsoft.com/f4f6c935-5207-46f6-b015-c4db724113f3">MI_Context_GetCustomOptionAt</a>.


#### - GetCustomOptionCount

Gets the count of defined provider custom options. See 
       <a href="https://msdn.microsoft.com/8cce1492-5c3a-4ba8-8f33-22f6ff7fcf3a">MI_Context_GetCustomOptionCount</a>.


#### - GetLocalSession

Gets the local session allowing the provider to communicate with the CIM server. See 
       <a href="https://msdn.microsoft.com/275657b1-9e74-456e-9ef9-28b621d27fc7">MI_Context_GetLocalSession</a>.


#### - GetLocale

Returns the locale of the given type. See 
       <a href="https://msdn.microsoft.com/7d2271e8-de76-4629-aedc-0ab882ab58eb">MI_Context_GetLocale</a>.


#### - GetNumberOption

Gets the specified provider custom option. See 
       <a href="https://msdn.microsoft.com/862a44b9-a6bd-4433-a7da-9309392a946c">MI_Context_GetNumberOption</a>.


#### - GetStringOption

Gets the specified provider custom option. See 
       <a href="https://msdn.microsoft.com/ef6fa103-7421-4c66-902d-c5a731abaa54">MI_Context_GetStringOption</a>.


#### - NewDynamicInstance

Creates a new dynamic instance of the class whose name is given by className. See 
       <a href="https://msdn.microsoft.com/05415945-c804-4056-b4bf-673995c1d6e4">MI_Context_NewDynamicInstance</a>.


#### - NewInstance

Creates a new instance of the class given by the classDecl parameter. See 
       <a href="https://msdn.microsoft.com/59571aa0-7fc2-4724-94e8-15b8a62327b6">MI_Context_NewInstance</a>.


#### - NewParameters

Creates a new instance of the method given by methodDecl. See 
       <a href="https://msdn.microsoft.com/8fb80e6f-627c-4897-9776-7454c0258809">MI_Context_NewParameters</a>.


#### - PostCimError

Posts a return code and an error message to the server in response to a request. See 
       <a href="https://msdn.microsoft.com/96ef9e97-467b-4b71-a7f9-4f640102e744">MI_Context_PostCimError</a>.


#### - PostError

Providers call this function to post a return code to the client in response to a request. See 
       <a href="https://msdn.microsoft.com/b52e3b28-a4b7-4017-9670-09b10363544b">MI_Context_PostError</a>.


#### - PostIndication

Posts an indication to the server in response to a request. See 
       <a href="https://msdn.microsoft.com/1e7fb986-0896-44cb-9b19-e3576911058c">MI_Context_PostIndication</a>.


#### - PostInstance

Providers call this function to post an instance to the server in response to a request. See 
       <a href="https://msdn.microsoft.com/b7c5e677-5b49-48b8-8273-4fd04c2f4a90">MI_Context_PostInstance</a>.


#### - PostResult

Providers call this function to post a return code to the server in response to a request. See 
       <a href="https://msdn.microsoft.com/e890ebab-f243-40eb-8a56-a771475929bb">MI_Context_PostResult</a>.


#### - PostTerminatingError

Posts a return code and an error message to the server in response to a request.


#### - PromptUser

Sends a prompt message to the client querying whether to continue the operation or cancel it. See 
       <a href="https://msdn.microsoft.com/ef50a509-20a8-482c-b7b9-0dc1f0ab4ee0">MI_Context_PromptUser</a>.


#### - RefuseUnload

Tells the provider infrastructure to not unload the provider. See 
       <a href="https://msdn.microsoft.com/d5d06ceb-5f44-4aa8-93a6-1c7b8d06561a">MI_Context_RefuseUnload</a>.


#### - RegisterCancel

Registers a callback that is invoked when the operation is canceled. See 
       <a href="https://msdn.microsoft.com/7e6b2016-6ce5-4dcd-b5f4-6e6d24c46f0a">MI_Context_RegisterCancel</a>.


#### - RequestUnload

Requests to unload the module or the provider (depending on the location of invocation). See 
       <a href="https://msdn.microsoft.com/1eb20bff-326d-4d2f-9b71-a14ca8975597">MI_Context_RequestUnload</a>.


#### - SetStringOption

Sets a context-specific option. See 
       <a href="https://msdn.microsoft.com/a7affdbe-1fc7-4662-8f21-077138365adf">MI_Context_SetStringOption</a>.


#### - ShouldContinue

Queries the client to determine if an operation should continue. See 
       <a href="https://msdn.microsoft.com/5548b75d-2d71-4ef1-828c-ae8fb5e9c165">MI_Context_ShouldContinue</a>.


#### - ShouldProcess

Queries the client to determine if an operation should continue. See 
       <a href="https://msdn.microsoft.com/adfa899c-f65a-4aac-b82d-5bc7b776713a">MI_Context_ShouldProcess</a>.


#### - WriteCimError

Sends a CIM error instance to the client. See 
       <a href="https://msdn.microsoft.com/6df0841b-3e13-4f9a-9e54-5c3c0c0d79fe">MI_Context_WriteCimError</a>.


#### - WriteError

This function has been deprecated. Use 
       <a href="https://msdn.microsoft.com/7626b488-58a3-4c9c-a80b-9b0a6dd7f533">MI_Context_WriteError</a> instead.

Sends an error code and error message to the client. See 
       <a href="https://msdn.microsoft.com/7626b488-58a3-4c9c-a80b-9b0a6dd7f533">MI_Context_WriteError</a>.


#### - WriteMessage

Sends an operational message to the client. See 
       <a href="https://msdn.microsoft.com/2e4dbb4d-5482-4ed0-9903-34b3bb87b16f">MI_Context_WriteMessage</a>.


#### - WriteProgress

Sends a progress message to the client. See 
       <a href="https://msdn.microsoft.com/260d46f3-b048-4278-acde-724323166ba2">MI_Context_WriteProgress</a>.


#### - WriteStreamParameter

Sends streamed parameter data to the requestor. See 
       <a href="https://msdn.microsoft.com/ae52a088-80da-404f-a453-9a9bea61edce">MI_Context_WriteStreamParameter</a>.

