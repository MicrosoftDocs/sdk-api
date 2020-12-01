---
UID: NS:mi._MI_ServerFT
title: MI_ServerFT (mi.h)
description: A support structure used in the MI_Server structure. Use the functions with the name prefix &quot;MI_Server_&quot; to manipulate these structures.
helpviewer_keywords: ["MI_ServerFT","MI_ServerFT structure [Windows Management Infrastructure (MI)]","mi/MI_ServerFT","wmi_v2.mi_serverft"]
old-location: wmi_v2\mi_serverft.htm
tech.root: wmi_v2
ms.assetid: a8b3b230-8378-448b-9c89-82b601373f0e
ms.date: 12/05/2018
ms.keywords: MI_ServerFT, MI_ServerFT structure [Windows Management Infrastructure (MI)], mi/MI_ServerFT, wmi_v2.mi_serverft
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
req.typenames: MI_ServerFT
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1,     Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
f1_keywords:
 - _MI_ServerFT
 - mi/_MI_ServerFT
 - MI_ServerFT
 - mi/MI_ServerFT
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
 - MI_ServerFT
---

## -description

A support structure used in the <a href="/windows/desktop/api/mi/ns-mi-mi_server">MI_Server</a> 
     structure. Use the functions with the name prefix "MI_Server_" to manipulate these structures.

## -struct-fields

### -field GetSystemName

Gets the system name for the server.

### -field GetVersion

Gets the value of the <b>MI_VERSION</b> macro used when compiling the server.
