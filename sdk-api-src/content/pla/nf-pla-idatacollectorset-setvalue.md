---
UID: NF:pla.IDataCollectorSet.SetValue
title: IDataCollectorSet::SetValue (pla.h)
description: Sets a user-defined value.
helpviewer_keywords: ["IDataCollectorSet interface [PLA]","SetValue method","IDataCollectorSet.SetValue","IDataCollectorSet::SetValue","SetValue","SetValue method [PLA]","SetValue method [PLA]","IDataCollectorSet interface","base.idatacollectorset_setvalue","pla.idatacollectorset_setvalue","pla/IDataCollectorSet::SetValue"]
old-location: pla\idatacollectorset_setvalue.htm
tech.root: PLA
ms.assetid: d2143de9-f189-47e0-8b28-0422d9984459
ms.date: 12/05/2018
ms.keywords: IDataCollectorSet interface [PLA],SetValue method, IDataCollectorSet.SetValue, IDataCollectorSet::SetValue, SetValue, SetValue method [PLA], SetValue method [PLA],IDataCollectorSet interface, base.idatacollectorset_setvalue, pla.idatacollectorset_setvalue, pla/IDataCollectorSet::SetValue
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
 - IDataCollectorSet::SetValue
 - pla/IDataCollectorSet::SetValue
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
 - IDataCollectorSet.SetValue
---

# IDataCollectorSet::SetValue


## -description

Sets a user-defined value.

## -parameters

### -param key [in]

The name of the value.

### -param value [in]

The value associated with the key.

## -returns

Returns S_OK if successful.

## -remarks

You can specify one or more user-defined values. If you specify a key that currently exists, the current value is overwritten. To remove a value, set the <i>pValue</i> parameter to <b>NULL</b>.

You use the key value if you want to perform variable substitution in the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_taskarguments">IDataCollectorSet::TaskArguments</a> property.

## -see-also

<a href="/previous-versions/windows/desktop/api/pla/nn-pla-idatacollectorset">IDataCollectorSet</a>



<a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-getvalue">IDataCollectorSet::GetValue</a>