---
UID: NF:mi.MI_Context_RefuseUnload
title: MI_Context_RefuseUnload function
author: windows-sdk-content
description: Tells the provider infrastructure not to unload the provider.
old-location: wmi_v2\mi_context_refuseunload.htm
tech.root: WMI_v2
ms.assetid: d5d06ceb-5f44-4aa8-93a6-1c7b8d06561a
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: MI_Context_RefuseUnload, MI_Context_RefuseUnload function [Windows Management Infrastructure (MI)], mi/MI_Context_RefuseUnload, wmi.mi_refuseunload, wmi_v2.mi_context_refuseunload
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
 - MI_Context_RefuseUnload
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
---

# MI_Context_RefuseUnload function


## -description


Tells the provider infrastructure not to unload the provider.


## -parameters




### -param context [in]

The request context.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.




## -remarks



This function stops the WMI server from shutting down the provider. The provider needs to call the <a href="https://msdn.microsoft.com/1eb20bff-326d-4d2f-9b71-a14ca8975597">MI_Context_RequestUnload</a> function to allow the provider to be unloaded, and that function must use the same context that was used with the <b>MI_Context_RefuseUnload</b> function.

Some providers may use this mechanism to cache expensive data; however, holding a provider open a provider that is rarely touched becomes a performance issue in the long term. A provider that wants to maintain control of the lifetime of its provider should use a decoupled provider. If the provider wants to hold it open for a couple of minutes to maintain caches more efficiently, and if no new requests are received within that time, it should then request unload to shut down the provider and potentially host.




## -see-also




<a href="https://msdn.microsoft.com/51d6c510-f9fd-4ab7-a669-b2a5776b496d">MI_Context</a>



<a href="https://msdn.microsoft.com/1eb20bff-326d-4d2f-9b71-a14ca8975597">MI_Context_RequestUnload</a>
 

 

