---
UID: NF:structuredquery.ISchemaProvider.SaveBinary
title: ISchemaProvider::SaveBinary
author: windows-sdk-content
description: Saves the loaded schema as a schema binary at a specified path.
old-location: search\_search_ISchemaProvider_SaveBinary.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\ischemaprovider\savebinary.htm
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: ISchemaProvider interface [search],SaveBinary method, ISchemaProvider.SaveBinary, ISchemaProvider::SaveBinary, SaveBinary, SaveBinary method [search], SaveBinary method [search],ISchemaProvider interface, _search_ISchemaProvider_SaveBinary, search._search_ISchemaProvider_SaveBinary, structuredquery/ISchemaProvider::SaveBinary
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: structuredquery.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Structuredquery.idl
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
 - COM
api_location:
 - Structuredquery.h
api_name:
 - ISchemaProvider.SaveBinary
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# ISchemaProvider::SaveBinary


## -description


Saves the loaded schema as a schema binary at a specified path.


## -parameters




### -param pszSchemaBinaryPath [in]

Type: <b>LPCWSTR</b>

Pointer to a null-terminated Unicode string that contains the fully qualified path at which to save the schema binary.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Any existing file at the location specified by <i>pszSchemaBinaryPath</i> is overwritten.



