---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# WS_SECURITY_HEADER_LAYOUT enumeration


## -description


The layout rules applied to the elements of the WS-Security
security header.  This setting is relevant to message security
bindings and mixed-mode security bindings.
            


## -enum-fields




### -field WS_SECURITY_HEADER_LAYOUT_STRICT


The elements of the security header must follow a 'declare before use'
layout.  All security tokens must appear before their usage.
                


### -field WS_SECURITY_HEADER_LAYOUT_LAX


The elements of the security header can be in arbitrary order,
including security tokens appearing after usage.
                


### -field WS_SECURITY_HEADER_LAYOUT_LAX_WITH_TIMESTAMP_FIRST


The elements of the security header can be in arbitrary order as in <a href="https://msdn.microsoft.com/a3090e6f-1f80-4d67-b7d7-1165486dcc66">WS_SECURITY_HEADER_LAYOUT_LAX</a>, but the timestamp element must
be the first element.
                


### -field WS_SECURITY_HEADER_LAYOUT_LAX_WITH_TIMESTAMP_LAST


The elements of the security header can be in arbitrary order as in <a href="https://msdn.microsoft.com/a3090e6f-1f80-4d67-b7d7-1165486dcc66">WS_SECURITY_HEADER_LAYOUT_LAX</a>, but the timestamp element must
be the last element.
                

