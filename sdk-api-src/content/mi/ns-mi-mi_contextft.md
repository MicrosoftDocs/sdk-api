---
UID: NS:mi._MI_ContextFT
title: MI_ContextFT (mi.h)

description: A support structure used in the MI_Context structure. Use the functions with the name prefix &#0034;MI_Context_&#0034; to manipulate these structures.
old-location: wmi_v2\mi_contextft.htm
tech.root: wmi_v2
ms.assetid: a5a3003f-9343-415d-b30f-32b479232db8

ms.date: 12/05/2018
ms.keywords: MI_ContextFT, MI_ContextFT structure [Windows Management Infrastructure (MI)], mi/MI_ContextFT, wmi_v2.mi_contextft
ms.topic: struct
f1_keywords:
- mi/MI_ContextFT
dev_langs:
 - c++
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
- MI_ContextFT
targetos: Windows
req.typenames: MI_ContextFT
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1,     Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
---

# MI_ContextFT structure


## -description


A support structure used in the <a href="https://docs.microsoft.com/windows/desktop/api/mi/ns-mi-mi_context">MI_Context</a> 
     structure. Use the functions with the name prefix "MI_Context_" to manipulate these 
     structures.


## -struct-fields




### -field MI_Result

TBD 




#### - Canceled

Determines whether the operation has been canceled. See 
       <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_context_canceled">MI_Context_Canceled</a>.


#### - ConstructInstance

Initializes an instance. See 
       <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_context_constructinstance">MI_Context_ConstructInstance</a>.


#### - ConstructParameters

Initialize a parameters instance. See 
       <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_context_constructparameters">MI_Context_ConstructParameters</a>.


#### - GetCustomOption

Gets the specified provider custom option. See 
       <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_context_getcustomoption">MI_Context_GetCustomOption</a>.


#### - GetCustomOptionAt

Gets the provider's custom option at the specified index. See 
       <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_context_getcustomoptionat">MI_Context_GetCustomOptionAt</a>.


#### - GetCustomOptionCount

Gets the count of defined provider custom options. See 
       <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_context_getcustomoptioncount">MI_Context_GetCustomOptionCount</a>.


#### - GetLocalSession

Gets the local session allowing the provider to communicate with the CIM server. See 
       <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_context_getlocalsession">MI_Context_GetLocalSession</a>.


#### - GetLocale

Returns the locale of the given type. See 
       <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_context_getlocale">MI_Context_GetLocale</a>.


#### - GetNumberOption

Gets the specified provider custom option. See 
       <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_context_getnumberoption">MI_Context_GetNumberOption</a>.


#### - GetStringOption

Gets the specified provider custom option. See 
       <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_context_getstringoption">MI_Context_GetStringOption</a>.


#### - NewDynamicInstance

Creates a new dynamic instance of the class whose name is given by className. See 
       <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_context_newdynamicinstance">MI_Context_NewDynamicInstance</a>.


#### - NewInstance

Creates a new instance of the class given by the classDecl parameter. See 
       <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_context_newinstance">MI_Context_NewInstance</a>.


#### - NewParameters

Creates a new instance of the method given by methodDecl. See 
       <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_context_newparameters">MI_Context_NewParameters</a>.


#### - PostCimError

Posts a return code and an error message to the server in response to a request. See 
       <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_context_postcimerror">MI_Context_PostCimError</a>.


#### - PostError

Providers call this function to post a return code to the client in response to a request. See 
       <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_context_posterror">MI_Context_PostError</a>.


#### - PostIndication

Posts an indication to the server in response to a request. See 
       <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_context_postindication">MI_Context_PostIndication</a>.


#### - PostInstance

Providers call this function to post an instance to the server in response to a request. See 
       <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_context_postinstance">MI_Context_PostInstance</a>.


#### - PostResult

Providers call this function to post a return code to the server in response to a request. See 
       <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_context_postresult">MI_Context_PostResult</a>.


#### - PostTerminatingError

Posts a return code and an error message to the server in response to a request.


#### - PromptUser

Sends a prompt message to the client querying whether to continue the operation or cancel it. See 
       <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_context_promptuser">MI_Context_PromptUser</a>.


#### - RefuseUnload

Tells the provider infrastructure to not unload the provider. See 
       <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_context_refuseunload">MI_Context_RefuseUnload</a>.


#### - RegisterCancel

Registers a callback that is invoked when the operation is canceled. See 
       <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_context_registercancel">MI_Context_RegisterCancel</a>.


#### - RequestUnload

Requests to unload the module or the provider (depending on the location of invocation). See 
       <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_context_requestunload">MI_Context_RequestUnload</a>.


#### - SetStringOption

Sets a context-specific option. See 
       <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_context_setstringoption">MI_Context_SetStringOption</a>.


#### - ShouldContinue

Queries the client to determine if an operation should continue. See 
       <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_context_shouldcontinue">MI_Context_ShouldContinue</a>.


#### - ShouldProcess

Queries the client to determine if an operation should continue. See 
       <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_context_shouldprocess">MI_Context_ShouldProcess</a>.


#### - WriteCimError

Sends a CIM error instance to the client. See 
       <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_context_writecimerror">MI_Context_WriteCimError</a>.


#### - WriteError

This function has been deprecated. Use 
       <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_context_writeerror">MI_Context_WriteError</a> instead.

Sends an error code and error message to the client. See 
       <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_context_writeerror">MI_Context_WriteError</a>.


#### - WriteMessage

Sends an operational message to the client. See 
       <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_context_writemessage">MI_Context_WriteMessage</a>.


#### - WriteProgress

Sends a progress message to the client. See 
       <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_context_writeprogress">MI_Context_WriteProgress</a>.


#### - WriteStreamParameter

Sends streamed parameter data to the requestor. See 
       <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_context_writestreamparameter">MI_Context_WriteStreamParameter</a>.

