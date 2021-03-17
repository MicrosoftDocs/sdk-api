---
UID: NF:wcmconfig.IItemEnumerator.Current
title: IItemEnumerator::Current (wcmconfig.h)
description: Retrieves an item from the current position of the enumerator.
helpviewer_keywords: ["Current","Current method [SMI]","Current method [SMI]","IItemEnumerator interface","IItemEnumerator interface [SMI]","Current method","IItemEnumerator.Current","IItemEnumerator::Current","smi.iitemenumerator_current","wcmconfig/IItemEnumerator::Current"]
old-location: smi\iitemenumerator_current.htm
tech.root: SMI
ms.assetid: 0f117274-672f-40da-a4c6-88dd6aa01cf7
ms.date: 12/05/2018
ms.keywords: Current, Current method [SMI], Current method [SMI],IItemEnumerator interface, IItemEnumerator interface [SMI],Current method, IItemEnumerator.Current, IItemEnumerator::Current, smi.iitemenumerator_current, wcmconfig/IItemEnumerator::Current
req.header: wcmconfig.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WcmConfig.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: SMIEngine.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IItemEnumerator::Current
 - wcmconfig/IItemEnumerator::Current
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SMIEngine.dll
api_name:
 - IItemEnumerator.Current
---

# IItemEnumerator::Current


## -description

Retrieves an item from the current position of the enumerator.

## -parameters

### -param Item [out]

A variant that contains the key value for the collection. For most collections, the key is the name of the item.

## -returns

This method returns an HRESULT value. <b>S_OK</b> indicates success.

## -remarks

<div class="alert"><b>Note</b>  When the item is no longer required, call <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear">VariantClear</a> to free the resources associated with the item.</div>
<div> </div>

## -see-also

<a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-iitemenumerator">IItemEnumerator</a>