---
UID: NS:mi._MI_Server
title: MI_Server (mi.h)
author: windows-sdk-content
description: This structure defines default function tables for all types:\_Context, Instance, PropertySet, and Filter.
old-location: wmi_v2\mi_server.htm
tech.root: wmi_v2
ms.assetid: bbe367c4-1964-4f6d-9345-fa19c090e018
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MI_Server, MI_Server structure [Windows Management Infrastructure (MI)], mi/MI_Server, wmi._mi_server, wmi_v2.mi_server
ms.topic: struct
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
 - MI_Server
product: Windows
targetos: Windows
req.typenames: MI_Server
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
---

# MI_Server structure


## -description


This structure defines default function tables
 for all types: Context, Instance, PropertySet, and Filter.


## -struct-fields




### -field serverFT

Pointer to an <b>MI_Server</b> function table.


### -field contextFT

Pointer to <a href="https://msdn.microsoft.com/51d6c510-f9fd-4ab7-a669-b2a5776b496d">MI_Context</a> function table.


### -field instanceFT

Pointer to <a href="https://msdn.microsoft.com/3dce1817-7995-49e5-8cc0-ee9496665e5c">MI_Instance</a> function table.


### -field propertySetFT

Pointer to <a href="https://msdn.microsoft.com/7c9e41b0-818e-46aa-8900-5006904f78d5">MI_PropertySet</a> function table.


### -field filterFT

Pointer to <a href="https://msdn.microsoft.com/0849cb55-ba2f-4855-ac33-fa96d8ecd94f">MI_Filter</a> function table.

