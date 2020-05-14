---
UID: NF:mi.MI_HostedProvider_GetApplication
title: MI_HostedProvider_GetApplication function (mi.h)
description: Gets the top-level application handle from which the hosted provider handle was created.helpviewer_keywords: ["MI_HostedProvider_GetApplication","MI_HostedProvider_GetApplication function [Windows Management Infrastructure (MI)]","mi/MI_HostedProvider_GetApplication","wmi_v2.mi_hostedprovider_getapplication"]
old-location: wmi_v2\mi_hostedprovider_getapplication.htm
tech.root: wmi_v2
ms.assetid: 26afde05-6ef6-4044-b8a1-fad2a3bb4385
ms.date: 12/05/2018
ms.keywords: MI_HostedProvider_GetApplication, MI_HostedProvider_GetApplication function [Windows Management Infrastructure (MI)], mi/MI_HostedProvider_GetApplication, wmi_v2.mi_hostedprovider_getapplication
f1_keywords:
- mi/MI_HostedProvider_GetApplication
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
- MI_HostedProvider_GetApplication
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
---

# MI_HostedProvider_GetApplication function


## -description


Gets the top-level application handle from which the hosted provider handle was created.


## -parameters




### -param hostedProvider [in]

Provider handle returned from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_newhostedprovider">MI_Application_NewHostedProvider</a>.


### -param application [out]

Returned application handle. This handle does not need to be deleted as it is a copy.


## -returns



A value of the <a href="https://docs.microsoft.com/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.



