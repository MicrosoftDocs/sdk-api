---
UID: NF:mi.MI_Context_RequestUnload
title: MI_Context_RequestUnload function (mi.h)
author: windows-sdk-content
description: Requests to unload the module or the provider.
old-location: wmi_v2\mi_context_requestunload.htm
tech.root: wmi_v2
ms.assetid: 1eb20bff-326d-4d2f-9b71-a14ca8975597
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: MI_Context_RequestUnload, MI_Context_RequestUnload function [Windows Management Infrastructure (MI)], mi/MI_Context_RequestUnload, wmi.mi_requestunload, wmi_v2.mi_context_requestunload
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
 - MI_Context_RequestUnload
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
---

# MI_Context_RequestUnload function


## -description


Requests to unload the module or the provider.


## -parameters




### -param context [in]

The request context.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.




## -remarks



This function undoes a call to the <a href="https://msdn.microsoft.com/d5d06ceb-5f44-4aa8-93a6-1c7b8d06561a">MI_Context_RefuseUnload</a> function. It must use the same context that was used in that function.




## -see-also




<a href="https://msdn.microsoft.com/51d6c510-f9fd-4ab7-a669-b2a5776b496d">MI_Context</a>



<a href="https://msdn.microsoft.com/d5d06ceb-5f44-4aa8-93a6-1c7b8d06561a">MI_Context_RefuseUnload</a>
 

 

