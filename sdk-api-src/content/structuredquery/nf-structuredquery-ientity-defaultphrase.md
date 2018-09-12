---
UID: NF:structuredquery.IEntity.DefaultPhrase
title: IEntity::DefaultPhrase
author: windows-sdk-content
description: Retrieves a default phrase to use for this entity in restatements.
old-location: search\_search_IEntity_DefaultPhrase.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\ientity\defaultphrase.htm
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: DefaultPhrase, DefaultPhrase method [search], DefaultPhrase method [search],IEntity interface, IEntity interface [search],DefaultPhrase method, IEntity.DefaultPhrase, IEntity::DefaultPhrase, _search_IEntity_DefaultPhrase, search._search_IEntity_DefaultPhrase, structuredquery/IEntity::DefaultPhrase
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
 - IEntity.DefaultPhrase
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# IEntity::DefaultPhrase


## -description


Retrieves a default phrase to use for this entity in restatements.
        


## -parameters




### -param ppszPhrase [out, retval]

Type: <b>LPWSTR*</b>

Receives a pointer to the default phrase as a Unicode string. The calling application must free the returned string by calling <a href="_com_CoTaskMemFree">CoTaskMemFree</a>.
              


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



