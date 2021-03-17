---
UID: NF:mi.MI_Server_GetSystemName
title: MI_Server_GetSystemName function (mi.h)
description: Gets the system name for the server.
helpviewer_keywords: ["MI_Server_GetSystemName","MI_Server_GetSystemName callback","MI_Server_GetSystemName callback function [Windows Management Infrastructure (MI)]","mi/MI_Server_GetSystemName","wmi_v2.mi_server_getsystemname"]
old-location: wmi_v2\mi_server_getsystemname.htm
tech.root: wmi_v2
ms.assetid: 895b21b8-dc66-4e05-9f10-9dcd704bef70
ms.date: 12/05/2018
ms.keywords: MI_Server_GetSystemName, MI_Server_GetSystemName callback, MI_Server_GetSystemName callback function [Windows Management Infrastructure (MI)], mi/MI_Server_GetSystemName, wmi_v2.mi_server_getsystemname
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
 - MI_Server_GetSystemName
 - mi/MI_Server_GetSystemName
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
 - MI_Server_GetSystemName
---

# MI_Server_GetSystemName function


## -description

Gets the system name for the server.

## -parameters

### -param systemName

Returned system name.

## -returns

This function returns MI_Result MI_CALL.

## -remarks

This function is only available from within a generated provider. It obtains the system name for this server. The system name is used in several standard CIM key properties (for example, CIM_Fan.SystemName). The name is only known by the server. The provider should use only this function to get the system name and should never attempt to determine the system name using other means. The system name is typically the host name for the system, but the server may add additional qualification.

