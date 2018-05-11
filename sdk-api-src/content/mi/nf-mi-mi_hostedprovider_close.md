---
UID: NF:mi.MI_HostedProvider_Close
title: MI_HostedProvider_Close function
author: windows-driver-content
description: Close a hosted provider handle that was returned from MI_Application_NewHostedProvider.
old-location: wmi_v2\mi_hostedprovider_close.htm
old-project: wmi_v2
ms.assetid: b0cae173-a552-4c5a-8181-ba20143d846b
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: MI_HostedProvider_Close, MI_HostedProvider_Close function [Windows Management Infrastructure (MI)], mi/MI_HostedProvider_Close, wmi_v2.mi_hostedprovider_close
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
req.typenames: MI_Type
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Mi.h
api_name:
-	MI_HostedProvider_Close
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_HostedProvider_Close function


## -description


Close a hosted provider handle that was returned from <a href="https://msdn.microsoft.com/4f39ffca-4ae3-4ce5-9460-c7ac27c06a50">MI_Application_NewHostedProvider</a>.


## -parameters




### -param hostedProvider [in, out]

A pointer to a provider handle returned from the <a href="https://msdn.microsoft.com/4f39ffca-4ae3-4ce5-9460-c7ac27c06a50">MI_Application_NewHostedProvider</a> function.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.




## -remarks



When this function returns, no new calls will enter the provider.




## -see-also




<a href="https://msdn.microsoft.com/4f39ffca-4ae3-4ce5-9460-c7ac27c06a50">MI_Application_NewHostedProvider</a>



<a href="https://msdn.microsoft.com/26afde05-6ef6-4044-b8a1-fad2a3bb4385">MI_HostedProvider_GetApplication</a>
 

 

