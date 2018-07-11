---
UID: NF:mi.MI_Context_PostResult
title: MI_Context_PostResult function
author: windows-sdk-content
description: Posts the final terminating result code back to the client (through the server) in response to a request.
old-location: wmi_v2\mi_context_postresult.htm
old-project: wmi_v2
ms.assetid: e890ebab-f243-40eb-8a56-a771475929bb
ms.author: windowssdkdev
ms.date: 06/14/2018
ms.keywords: MI_Context_PostResult, MI_Context_PostResult function [Windows Management Infrastructure (MI)], mi/MI_Context_PostResult, wmi.mi_postresult, wmi_v2.mi_context_postresult
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
 - MI_Context_PostResult
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_Context_PostResult function


## -description


Posts the final terminating result code back to the client (through the server) in response to a request.


## -parameters




### -param context [in]

Request context.


### -param result

Result code to post to the server.


## -returns



This function returns MI_INLINE MI_Result MI_INLINE_CALL.




## -remarks



All calls to the <a href="https://msdn.microsoft.com/1e7fb986-0896-44cb-9b19-e3576911058c">MI_Context_PostIndication</a> and <a href="https://msdn.microsoft.com/b7c5e677-5b49-48b8-8273-4fd04c2f4a90">MI_Context_PostInstance</a> functions must be complete before calling this function. When this function is called, the lifetime of the request context is terminated; the context becomes invalid, and no additional calls can be made on the context.




## -see-also




<a href="https://msdn.microsoft.com/51d6c510-f9fd-4ab7-a669-b2a5776b496d">MI_Context</a>



<a href="https://msdn.microsoft.com/1e7fb986-0896-44cb-9b19-e3576911058c">MI_Context_PostIndication</a>



<a href="https://msdn.microsoft.com/b7c5e677-5b49-48b8-8273-4fd04c2f4a90">MI_Context_PostInstance</a>
 

 

