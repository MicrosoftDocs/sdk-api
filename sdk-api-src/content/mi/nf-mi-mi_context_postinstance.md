---
UID: NF:mi.MI_Context_PostInstance
title: MI_Context_PostInstance function
author: windows-sdk-content
description: Posts an instance back to the client (through the server) in response to a request.
old-location: wmi_v2\mi_context_postinstance.htm
tech.root: WMI_v2
ms.assetid: b7c5e677-5b49-48b8-8273-4fd04c2f4a90
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: MI_Context_PostInstance, MI_Context_PostInstance function [Windows Management Infrastructure (MI)], mi/MI_Context_PostInstance, wmi.mi_postinstance, wmi_v2.mi_context_postinstance
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
 - MI_Context_PostInstance
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
---

# MI_Context_PostInstance function


## -description


Posts an instance back to the client (through the server) in response to a request.


## -parameters




### -param context [in]

Request context.


### -param instance [in]

Instance to be posted to the server.


## -returns



This function returns MI_INLINE MI_Result MI_INLINE_CALL.




## -remarks



There will be posting functions automatically generated for the indication class (for example, className_Post), and they should be called here.

The server is responsible for copying the instance so the provider is free to dispose of the instance afterwards using the <a href="https://msdn.microsoft.com/6370e464-b262-4c91-a3c8-889911df7965">MI_Instance_Delete</a> function.




## -see-also




<a href="https://msdn.microsoft.com/51d6c510-f9fd-4ab7-a669-b2a5776b496d">MI_Context</a>



<a href="https://msdn.microsoft.com/3dce1817-7995-49e5-8cc0-ee9496665e5c">MI_Instance</a>



<a href="https://msdn.microsoft.com/6370e464-b262-4c91-a3c8-889911df7965">MI_Instance_Delete</a>
 

 

