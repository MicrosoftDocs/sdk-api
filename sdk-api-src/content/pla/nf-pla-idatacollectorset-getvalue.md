---
UID: NF:pla.IDataCollectorSet.GetValue
title: IDataCollectorSet::GetValue (pla.h)
description: Retrieves a user-defined value.
helpviewer_keywords: ["GetValue","GetValue method [PLA]","GetValue method [PLA]","IDataCollectorSet interface","IDataCollectorSet interface [PLA]","GetValue method","IDataCollectorSet.GetValue","IDataCollectorSet::GetValue","base.idatacollectorset_getvalue","pla.idatacollectorset_getvalue","pla/IDataCollectorSet::GetValue"]
old-location: pla\idatacollectorset_getvalue.htm
tech.root: PLA
ms.assetid: 0f82e154-7d3f-44c9-8bdd-cc1522499e85
ms.date: 12/05/2018
ms.keywords: GetValue, GetValue method [PLA], GetValue method [PLA],IDataCollectorSet interface, IDataCollectorSet interface [PLA],GetValue method, IDataCollectorSet.GetValue, IDataCollectorSet::GetValue, base.idatacollectorset_getvalue, pla.idatacollectorset_getvalue, pla/IDataCollectorSet::GetValue
req.header: pla.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: Pla.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDataCollectorSet::GetValue
 - pla/IDataCollectorSet::GetValue
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Pla.dll
api_name:
 - IDataCollectorSet.GetValue
---

# IDataCollectorSet::GetValue


## -description

Retrieves a user-defined value.

## -parameters

### -param key [in]

The key of the value to retrieve.

### -param value [out]

A value associated with the key.

## -returns

Returns S_OK if successful.

## -see-also

<a href="/previous-versions/windows/desktop/api/pla/nn-pla-idatacollectorset">IDataCollectorSet</a>



<a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-setvalue">IDataCollectorSet::SetValue</a>