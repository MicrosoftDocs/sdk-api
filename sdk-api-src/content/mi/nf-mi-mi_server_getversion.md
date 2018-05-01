---
UID: NF:mi.MI_Server_GetVersion
title: MI_Server_GetVersion function
author: windows-driver-content
description: Gets the value of the MI_VERSION macro used when generating the provider.
old-location: wmi_v2\mi_server_getversion.htm
old-project: wmi_v2
ms.assetid: ba3d3bc8-fd07-45c7-8292-38768738cf82
ms.author: windowsdriverdev
ms.date: 4/18/2018
ms.keywords: MI_Server_GetVersion, MI_Server_GetVersion callback function [Windows Management Infrastructure (MI)], mi/MI_Server_GetVersion, wmi_v2.mi_server_getversion
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
-	UserDefined
api_location:
-	Mi.h
api_name:
-	MI_Server_GetVersion
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
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



