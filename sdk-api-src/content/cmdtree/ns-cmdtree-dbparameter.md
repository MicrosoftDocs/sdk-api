---
UID: NS:cmdtree.tagDBPARAMETER
title: DBPARAMETER (cmdtree.h)
description: The DBPARAMETER structure is used to define values for scalar parameters.
helpviewer_keywords: ["DBPARAMETER","DBPARAMETER structure [Indexing Service]","_idxs_DBPARAMETER","cmdtree/DBPARAMETER","indexsrv.dbparameter","tagDBPARAMETER"]
old-location: indexsrv\dbparameter.htm
tech.root: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixoledb_2p0y.htm
ms.date: 12/05/2018
ms.keywords: DBPARAMETER, DBPARAMETER structure [Indexing Service], _idxs_DBPARAMETER, cmdtree/DBPARAMETER, indexsrv.dbparameter, tagDBPARAMETER
req.header: cmdtree.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: DBPARAMETER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagDBPARAMETER
 - cmdtree/tagDBPARAMETER
 - DBPARAMETER
 - cmdtree/DBPARAMETER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - cmdtree.h
api_name:
 - DBPARAMETER
---

# DBPARAMETER structure


## -description

> [!Note]  
> Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use [Windows Search](/windows/desktop/search/-search-3x-wds-overview) for client side search and [Microsoft Search Server Express](https://www.microsoft.com/download/details.aspx?id=18914) for server side search.

The <b>DBPARAMETER</b> structure is used to define values for scalar parameters.

## -struct-fields

### -field pwszName

parameter name

### -field pTypeInfo

if not a null pointer, type is described
                             by the ITypeInfo

### -field pNum

 Structure describing the
                             precision, scale and value of the numeric value.

### -field cbMaxLength

the maximum length of the parameter

### -field dwFlags

bitmask describing parameter characteristics

### -field wType

type of the parameter

## -remarks

Note that there is no entry for the ordinal position of the parameter. The assumption is that the ordinal position will be determined by the provider after evaluating the tree as a whole, and not by assigning a specific value to an individual member within the tree. Data consumers can determine the ordinal position based on the name using <b>ICommandWithParameters::MapParameterNames</b>. For more information about the interface, see <a href="/previous-versions/windows/desktop/ms712937(v=vs.85)">ICommandWithParameters</a>.