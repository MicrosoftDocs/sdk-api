---
UID: NF:mi.MI_Context_PostCimError
title: MI_Context_PostCimError function
author: windows-sdk-content
description: Posts a return code and an error message (in the form of a CIM_Error object) to the server in response to a request.
old-location: wmi_v2\mi_context_postcimerror.htm
old-project: wmi_v2
ms.assetid: 96ef9e97-467b-4b71-a7f9-4f640102e744
ms.author: windowssdkdev
ms.date: 08/13/2018
ms.keywords: MI_Context_PostCimError, MI_Context_PostCimError function [Windows Management Infrastructure (MI)], mi/MI_Context_PostCimError, wmi.mi_postcimerror, wmi_v2.mi_context_postcimerror
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
 - MI_Context_PostCimError
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_Context_PostCimError function


## -description


Posts a return code and an error message (in the form of a <a href="https://msdn.microsoft.com/e57636aa-6e04-4159-8fe1-5cc14d193891">CIM_Error</a> object) to the server in response to a request.


## -parameters




### -param context [in]

A pointer to the request context.


### -param error [in]

A pointer to a <a href="https://msdn.microsoft.com/e57636aa-6e04-4159-8fe1-5cc14d193891">CIM_Error</a> object to be posted to the server.


## -returns



This function returns MI_INLINE MI_Result MI_INLINE_CALL.




## -remarks



The <a href="https://msdn.microsoft.com/e57636aa-6e04-4159-8fe1-5cc14d193891">CIM_Error</a> instance that is returned in the <i>error</i> parameter can be compiled into your provider so you can initialize and then post it. Once an error has been posted, the context must not be used, as it becomes invalid at this point.




## -see-also




<a href="https://msdn.microsoft.com/e57636aa-6e04-4159-8fe1-5cc14d193891">CIM_Error</a>



<a href="https://msdn.microsoft.com/51d6c510-f9fd-4ab7-a669-b2a5776b496d">MI_Context</a>



<a href="https://msdn.microsoft.com/6df0841b-3e13-4f9a-9e54-5c3c0c0d79fe">MI_Context_WriteCimError</a>



<a href="https://msdn.microsoft.com/3dce1817-7995-49e5-8cc0-ee9496665e5c">MI_Instance</a>
 

 

