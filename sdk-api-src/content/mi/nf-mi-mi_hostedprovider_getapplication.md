---
UID: NF:mi.MI_HostedProvider_GetApplication
title: MI_HostedProvider_GetApplication function
author: windows-sdk-content
description: Gets the top-level application handle from which the hosted provider handle was created.
old-location: wmi_v2\mi_hostedprovider_getapplication.htm
tech.root: wmi_v2
ms.assetid: 26afde05-6ef6-4044-b8a1-fad2a3bb4385
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: MI_HostedProvider_GetApplication, MI_HostedProvider_GetApplication function [Windows Management Infrastructure (MI)], mi/MI_HostedProvider_GetApplication, wmi_v2.mi_hostedprovider_getapplication
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
 - MI_HostedProvider_GetApplication
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
---

# MI_HostedProvider_GetApplication function


## -description


Gets the top-level application handle from which the hosted provider handle was created.


## -parameters




### -param hostedProvider [in]

Provider handle returned from <a href="https://msdn.microsoft.com/4f39ffca-4ae3-4ce5-9460-c7ac27c06a50">MI_Application_NewHostedProvider</a>.


### -param application [out]

Returned application handle. This handle does not need to be deleted as it is a copy.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.



