---
UID: NF:mi.MI_Server_GetVersion
title: MI_Server_GetVersion function (mi.h)
description: Gets the value of the MI_VERSION macro used when generating the provider.
helpviewer_keywords: ["MI_Server_GetVersion","MI_Server_GetVersion callback","MI_Server_GetVersion callback function [Windows Management Infrastructure (MI)]","mi/MI_Server_GetVersion","wmi_v2.mi_server_getversion"]
old-location: wmi_v2\mi_server_getversion.htm
tech.root: wmi_v2
ms.assetid: ba3d3bc8-fd07-45c7-8292-38768738cf82
ms.date: 12/05/2018
ms.keywords: MI_Server_GetVersion, MI_Server_GetVersion callback, MI_Server_GetVersion callback function [Windows Management Infrastructure (MI)], mi/MI_Server_GetVersion, wmi_v2.mi_server_getversion
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
 - MI_Server_GetVersion
 - mi/MI_Server_GetVersion
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Mi.h
api_name:
 - MI_Server_GetVersion
---

# MI_Server_GetVersion function


## -description

Gets the value of the MI_VERSION macro used when generating the provider.

## -parameters

### -param version

Returned version number.

## -returns

This function returns MI_Result MI_CALL.

## -remarks

This function is only available inside a generated provider.

