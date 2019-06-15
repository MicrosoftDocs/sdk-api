---
UID: NF:structuredquery.IEntity.Name
title: IEntity::Name (structuredquery.h)
author: windows-sdk-content
description: Retrieves the name of this entity.
old-location: search\_search_IEntity_Name.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\ientity\name.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IEntity interface [search],Name method, IEntity.Name, IEntity::Name, Name, Name method [search], Name method [search],IEntity interface, _search_IEntity_Name, search._search_IEntity_Name, structuredquery/IEntity::Name
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
 - IEntity.Name
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
---

# IEntity::Name


## -description


Retrieves the name of this entity.
        


## -parameters




### -param ppszName [out, retval]

Type: <b>LPWSTR*</b>

Receives a pointer to the name of this entity as a Unicode string. The calling application must free the returned string by calling <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>. 
            


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Each name must be unique.



