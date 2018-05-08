---
UID: NS:searchapi._TIMEOUT_INFO
title: "_TIMEOUT_INFO"
author: windows-driver-content
description: Stores time-out values for connections and data.
old-location: search\_search_TIMEOUT_INFO.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\structures\timeout_info.htm
ms.author: windowsdriverdev
ms.date: 5/4/2018
ms.keywords: TIMEOUT_INFO, TIMEOUT_INFO structure [search], _TIMEOUT_INFO, _search_TIMEOUT_INFO, search._search_TIMEOUT_INFO, searchapi/TIMEOUT_INFO
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: searchapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Srchprth.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TIMEOUT_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Searchapi.h
api_name:
-	TIMEOUT_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# _TIMEOUT_INFO structure


## -description


Stores time-out values for connections and data.


## -struct-fields




### -field dwSize

Type: <b>DWORD</b>

The size of the structure, in bytes.


### -field dwConnectTimeout

Type: <b>DWORD</b>

The time-out value for a connection, in seconds.


### -field dwDataTimeout

Type: <b>DWORD</b>

The time-out value for data, in seconds.

