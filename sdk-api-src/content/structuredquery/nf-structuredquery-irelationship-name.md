---
UID: NF:structuredquery.IRelationship.Name
title: IRelationship::Name
author: windows-sdk-content
description: Retrieves the name of the relationship.
old-location: search\_search_IRelationship_Name.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\irelationship\name.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IRelationship interface [search],Name method, IRelationship.Name, IRelationship::Name, Name, Name method [search], Name method [search],IRelationship interface, _search_IRelationship_Name, search._search_IRelationship_Name, structuredquery/IRelationship::Name
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
 - IRelationship.Name
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
- apiref
: 
- COM
: 
- structuredquery.h
: 
- IRelationship.Name
: 
---

# IRelationship::Name


## -description


Retrieves the name of the relationship.
      


## -parameters




### -param ppszName [out, retval]

Type: <b>LPWSTR*</b>

Receives a pointer to the name of the relationship as a Unicode string. The calling application must free the returned string by calling <a href="_com_CoTaskMemFree">CoTaskMemFree</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



