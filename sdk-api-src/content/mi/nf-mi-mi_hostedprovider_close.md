---
UID: NF:mi.MI_HostedProvider_Close
title: MI_HostedProvider_Close function (mi.h)
description: Close a hosted provider handle that was returned from MI_Application_NewHostedProvider.
helpviewer_keywords: ["MI_HostedProvider_Close","MI_HostedProvider_Close function [Windows Management Infrastructure (MI)]","mi/MI_HostedProvider_Close","wmi_v2.mi_hostedprovider_close"]
old-location: wmi_v2\mi_hostedprovider_close.htm
tech.root: wmi_v2
ms.assetid: b0cae173-a552-4c5a-8181-ba20143d846b
ms.date: 12/05/2018
ms.keywords: MI_HostedProvider_Close, MI_HostedProvider_Close function [Windows Management Infrastructure (MI)], mi/MI_HostedProvider_Close, wmi_v2.mi_hostedprovider_close
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
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
f1_keywords:
 - MI_HostedProvider_Close
 - mi/MI_HostedProvider_Close
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mi.h
api_name:
 - MI_HostedProvider_Close
---

# MI_HostedProvider_Close function


## -description

Close a hosted provider handle that was returned from <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_newhostedprovider">MI_Application_NewHostedProvider</a>.

## -parameters

### -param hostedProvider [in, out]

A pointer to a provider handle returned from the <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_newhostedprovider">MI_Application_NewHostedProvider</a> function.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.

## -remarks

When this function returns, no new calls will enter the provider.

## -see-also

<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_newhostedprovider">MI_Application_NewHostedProvider</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_hostedprovider_getapplication">MI_HostedProvider_GetApplication</a>