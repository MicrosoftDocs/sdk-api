---
UID: NF:mi.MI_Context_PostIndication
title: MI_Context_PostIndication function
author: windows-sdk-content
description: Posts an indication result to the server in response to a subscribe operation request.
old-location: wmi_v2\mi_context_postindication.htm
tech.root: WMI_v2
ms.assetid: 1e7fb986-0896-44cb-9b19-e3576911058c
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: MI_Context_PostIndication, MI_Context_PostIndication function [Windows Management Infrastructure (MI)], mi/MI_Context_PostIndication, wmi.mi_postindication, wmi_v2.mi_context_postindication
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - MI_Context_PostIndication
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
---

# MI_Context_PostIndication function


## -description


Posts an indication result to the server in response to a subscribe operation request.


## -parameters




### -param context [in]

Request context.


### -param indication [in]

Indication instance to be posted.


### -param subscriptionIDCount

Number of subscription identifiers.


### -param bookmark

An optional, null-terminated string that represents the bookmark for this subscription. In general, if a bookmark was supplied to the subscribe operation, and bookmarks are supported, a resume bookmark should be returned with every indication.


## -returns



This function returns MI_INLINE MI_Result MI_INLINE_CALL.




## -remarks



There will be posting functions automatically generated for the indication class (for example, className_Post).

The server is responsible for copying the instance so the provider is free to dispose of the instance afterwards using the <a href="https://msdn.microsoft.com/6370e464-b262-4c91-a3c8-889911df7965">MI_Instance_Delete</a> function.




## -see-also




<a href="https://msdn.microsoft.com/51d6c510-f9fd-4ab7-a669-b2a5776b496d">MI_Context</a>



<a href="https://msdn.microsoft.com/3dce1817-7995-49e5-8cc0-ee9496665e5c">MI_Instance</a>



<a href="https://msdn.microsoft.com/6370e464-b262-4c91-a3c8-889911df7965">MI_Instance_Delete</a>
 

 

