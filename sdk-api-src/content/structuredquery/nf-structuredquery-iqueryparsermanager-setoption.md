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

# IQueryParserManager::SetOption


## -description


Changes a single option in this <a href="https://msdn.microsoft.com/ff1941e1-03f0-4fdb-a34b-61da4055f569">IQueryParserManager</a> object. For example, this method could change the name of the schema binary to load or the location of localized schema binaries.


## -parameters




### -param option [in]

Type: <b><a href="https://msdn.microsoft.com/ad19e452-f457-4cd6-9d41-c9a61d94a685">QUERY_PARSER_MANAGER_OPTION</a></b>

The <a href="https://msdn.microsoft.com/ad19e452-f457-4cd6-9d41-c9a61d94a685">QUERY_PARSER_MANAGER_OPTION</a> to be changed.


### -param pOptionValue [in]

Type: <b>PROPVARIANT const*</b>

A pointer to the value to use for the option selected.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



