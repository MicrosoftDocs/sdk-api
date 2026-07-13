---
UID: NF:sbtsv.ITsSbGlobalStore.EnumerateFarms
title: ITsSbGlobalStore::EnumerateFarms (sbtsv.h)
description: Enumerates all the farms that have been added by the specified resource plug-in.
helpviewer_keywords: ["EnumerateFarms","EnumerateFarms method [Remote Desktop Services]","EnumerateFarms method [Remote Desktop Services]","ITsSbGlobalStore interface","ITsSbGlobalStore interface [Remote Desktop Services]","EnumerateFarms method","ITsSbGlobalStore.EnumerateFarms","ITsSbGlobalStore::EnumerateFarms","sbtsv/ITsSbGlobalStore::EnumerateFarms","termserv.itssbglobalstore_enumeratefarms"]
old-location: termserv\itssbglobalstore_enumeratefarms.htm
tech.root: TermServ
ms.assetid: 51c59f35-667c-4723-aa7b-e8250bbdabe9
ms.date: 12/05/2018
ms.keywords: EnumerateFarms, EnumerateFarms method [Remote Desktop Services], EnumerateFarms method [Remote Desktop Services],ITsSbGlobalStore interface, ITsSbGlobalStore interface [Remote Desktop Services],EnumerateFarms method, ITsSbGlobalStore.EnumerateFarms, ITsSbGlobalStore::EnumerateFarms, sbtsv/ITsSbGlobalStore::EnumerateFarms, termserv.itssbglobalstore_enumeratefarms
req.header: sbtsv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Sbtsv.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITsSbGlobalStore::EnumerateFarms
 - sbtsv/ITsSbGlobalStore::EnumerateFarms
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sbtsv.h
api_name:
 - ITsSbGlobalStore.EnumerateFarms
---

# ITsSbGlobalStore::EnumerateFarms


## -description

Enumerates all the farms that have been added by the specified resource 
plug-in.

## -parameters

### -param ProviderName [in]

The provider name of the resource plug-in.

### -param pdwCount [out]

The count of farms retrieved.

### -param pVal [out]

A pointer to an array of farm names. The number of elements in this array is specified by the <i>pdwCount</i> parameter. When you have finished using the array, free the allocated memory by calling the <a href="/windows/desktop/api/oleauto/nf-oleauto-safearraydestroy">SafeArrayDestroy</a> function.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbglobalstore">ITsSbGlobalStore</a>