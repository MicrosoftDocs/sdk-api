---
UID: NF:fhcfg.IFhScopeIterator.MoveToNextItem
title: IFhScopeIterator::MoveToNextItem (fhcfg.h)
description: Moves to the next item in the inclusion or exclusion list.
helpviewer_keywords: ["IFhScopeIterator interface [Windows API]","MoveToNextItem method","IFhScopeIterator.MoveToNextItem","IFhScopeIterator::MoveToNextItem","MoveToNextItem","MoveToNextItem method [Windows API]","MoveToNextItem method [Windows API]","IFhScopeIterator interface","fhcfg/IFhScopeIterator::MoveToNextItem","winprog.ifhscopeiterator_movetonextitem"]
old-location: winprog\ifhscopeiterator_movetonextitem.htm
tech.root: winprog
ms.assetid: FD8B5460-FBD7-47D3-ADB0-DB3D6AB5A51A
ms.date: 12/05/2018
ms.keywords: IFhScopeIterator interface [Windows API],MoveToNextItem method, IFhScopeIterator.MoveToNextItem, IFhScopeIterator::MoveToNextItem, MoveToNextItem, MoveToNextItem method [Windows API], MoveToNextItem method [Windows API],IFhScopeIterator interface, fhcfg/IFhScopeIterator::MoveToNextItem, winprog.ifhscopeiterator_movetonextitem
req.header: fhcfg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Fhcfg.idl
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
 - IFhScopeIterator::MoveToNextItem
 - fhcfg/IFhScopeIterator::MoveToNextItem
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fhcfg.h
api_name:
 - IFhScopeIterator.MoveToNextItem
---

# IFhScopeIterator::MoveToNextItem


## -description

Moves to the next item in the inclusion or exclusion list.

> [!NOTE] 
> **IFhScopeIterator** is deprecated and may be altered or unavailable in future releases.



## -returns

<b>S_OK</b> on success, or an unsuccessful <b>HRESULT</b> on failure. Possible unsuccessful <b>HRESULT</b> values include values defined in the FhErrors.h header file.

## -remarks

If the current item is the last item in the list, or if the list is empty, this method returns <code>HRESULT_FROM_WIN32(ERROR_NOT_FOUND)</code>.

## -see-also

<a href="/windows/desktop/api/fhcfg/nn-fhcfg-ifhscopeiterator">IFhScopeIterator</a>



<a href="/windows/desktop/api/fhcfg/nf-fhcfg-ifhscopeiterator-getitem">IFhScopeIterator::GetItem</a>
