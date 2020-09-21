---
UID: NF:filehc.AssociateContextWithName
title: AssociateContextWithName function (filehc.h)
description: Inserts a name into the name cache to find a specified FIO_CONTEXT structure.
helpviewer_keywords: ["AssociateContextWithName","AssociateContextWithName function [Windows API]","filehc/AssociateContextWithName","winprog._associatecontextwithname"]
old-location: winprog\_associatecontextwithname.htm
tech.root: winprog
ms.assetid: 4f4bbfda-3be0-41d3-9087-d46edd2e21a3
ms.date: 12/05/2018
ms.keywords: AssociateContextWithName, AssociateContextWithName function [Windows API], filehc/AssociateContextWithName, winprog._associatecontextwithname
req.header: filehc.h
req.include-header: 
req.target-type: Windows
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
req.lib: Fcachdll.lib
req.dll: Fcachdll.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AssociateContextWithName
 - filehc/AssociateContextWithName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Fcachdll.dll
api_name:
 - AssociateContextWithName
---

# AssociateContextWithName function


## -description

Inserts a name into the name cache to find a specified <a href="/previous-versions/exchange-server/exchange-10/ms528326(v=exchg.10)">FIO_CONTEXT</a> structure.

## -parameters

### -param pNameCache [in]

A pointer to the name of the cache to be used.

### -param lpbName [in]

User-specified bytes for the name of the cache item.

### -param cbName [in]

The length of the name that is assigned to the cache item.

### -param lpbData [in]

User-specified bytes for any arbitrary data to associate with the name of the cache item.

### -param cbData [in]

The length, in bytes, of arbitrary data to associate with the name.

### -param pGenericMapping [in]

A pointer to a <a href="/windows/desktop/api/winnt/ns-winnt-generic_mapping">GENERIC_MAPPING</a> structure to associate with the name.

### -param pSecurityDescriptor [in]

The self-relative security descriptor to be associated with the name. This descriptor is provided by the user.

### -param pContext [in]

A pointer to an <a href="/previous-versions/exchange-server/exchange-10/ms528326(v=exchg.10)">FIO_CONTEXT</a> structure.

### -param fKeepReference [in]

Specifies whether the reference on the <a href="/previous-versions/exchange-server/exchange-10/ms528326(v=exchg.10)">FIO_CONTEXT</a> structure should be kept. If set to <b>TRUE</b>, the reference is kept.

## -returns

Returns <b>TRUE</b> if the function succeeds; otherwise, it returns <b>FALSE</b>.

## -remarks

If the name is already present in the cache, this call fails and <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns ERROR_DUP_NAME.

## -see-also

<a href="/previous-versions/exchange-server/exchange-10/ms528326(v=exchg.10)">FIO_CONTEXT</a>



<a href="/windows/desktop/api/winnt/ns-winnt-generic_mapping">GENERIC_MAPPING</a>