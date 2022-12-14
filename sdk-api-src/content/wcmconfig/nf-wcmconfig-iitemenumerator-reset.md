---
UID: NF:wcmconfig.IItemEnumerator.Reset
title: IItemEnumerator::Reset (wcmconfig.h)
description: Resets the state of the enumerator to its initialized state. You must immediately follow IItemEnumerator::Reset with a call to IItemEnumerator::MoveNext on the enumerator in order to set the current pointer at the first position in the enumeration.
helpviewer_keywords: ["IItemEnumerator interface [SMI]","Reset method","IItemEnumerator.Reset","IItemEnumerator::Reset","Reset","Reset method [SMI]","Reset method [SMI]","IItemEnumerator interface","smi.iitemenumerator_reset","wcmconfig/IItemEnumerator::Reset"]
old-location: smi\iitemenumerator_reset.htm
tech.root: SMI
ms.assetid: 6da5d581-7f8c-48fa-8522-1e51a805ad9b
ms.date: 12/05/2018
ms.keywords: IItemEnumerator interface [SMI],Reset method, IItemEnumerator.Reset, IItemEnumerator::Reset, Reset, Reset method [SMI], Reset method [SMI],IItemEnumerator interface, smi.iitemenumerator_reset, wcmconfig/IItemEnumerator::Reset
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
 - IItemEnumerator::Reset
 - wcmconfig/IItemEnumerator::Reset
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
 - IItemEnumerator.Reset
---

# IItemEnumerator::Reset


## -description

Resets the state of the enumerator to its initialized state. You must immediately follow <b>IItemEnumerator::Reset</b> with a call  to  <a href="/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-iitemenumerator-movenext">IItemEnumerator::MoveNext</a> on the enumerator   in order to set the current pointer at the first position in the enumeration.



## -returns

This method returns an HRESULT value. <b>S_OK</b> indicates success.

## -see-also

<a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-iitemenumerator">IItemEnumerator</a>
