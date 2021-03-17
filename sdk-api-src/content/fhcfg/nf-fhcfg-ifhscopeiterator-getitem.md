---
UID: NF:fhcfg.IFhScopeIterator.GetItem
title: IFhScopeIterator::GetItem (fhcfg.h)
description: Retrieves the current item in an inclusion or exclusion list.
helpviewer_keywords: ["GetItem","GetItem method [Windows API]","GetItem method [Windows API]","IFhScopeIterator interface","IFhScopeIterator interface [Windows API]","GetItem method","IFhScopeIterator.GetItem","IFhScopeIterator::GetItem","fhcfg/IFhScopeIterator::GetItem","winprog.ifhscopeiterator_getitem"]
old-location: winprog\ifhscopeiterator_getitem.htm
tech.root: winprog
ms.assetid: EB732725-497C-4D58-A05C-373732054BE5
ms.date: 12/05/2018
ms.keywords: GetItem, GetItem method [Windows API], GetItem method [Windows API],IFhScopeIterator interface, IFhScopeIterator interface [Windows API],GetItem method, IFhScopeIterator.GetItem, IFhScopeIterator::GetItem, fhcfg/IFhScopeIterator::GetItem, winprog.ifhscopeiterator_getitem
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
 - IFhScopeIterator::GetItem
 - fhcfg/IFhScopeIterator::GetItem
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
 - IFhScopeIterator.GetItem
---

# IFhScopeIterator::GetItem


## -description

Retrieves the current item in an inclusion or exclusion list.

> [!NOTE] 
> **IFhScopeIterator** is deprecated and may be altered or unavailable in future releases.

## -parameters

### -param Item [out]

This parameter must be <b>NULL</b> on input. On output, it receives a pointer to a string that contains the current element of the list. This element is a library name or a folder name, depending on the parameters that were passed to the <a href="/windows/desktop/api/fhcfg/nf-fhcfg-ifhconfigmgr-getincludeexcluderules">IFhConfigMgr::GetIncludeExcludeRules</a> method. The string is allocated by calling <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring">SysAllocString</a>. You must call <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> to free the string when it is no longer needed.

## -returns

<b>S_OK</b> on success, or an unsuccessful <b>HRESULT</b> on failure. Possible unsuccessful <b>HRESULT</b> values include values defined in the FhErrors.h header file.

## -remarks

To move to the next item in the inclusion or exclusion list, call the <a href="/windows/desktop/api/fhcfg/nf-fhcfg-ifhscopeiterator-movetonextitem">IFhScopeIterator::MoveToNextItem</a> method.

## -see-also

<a href="/windows/desktop/api/fhcfg/nn-fhcfg-ifhscopeiterator">IFhScopeIterator</a>



<a href="/windows/desktop/api/fhcfg/nf-fhcfg-ifhscopeiterator-movetonextitem">IFhScopeIterator::MoveToNextItem</a>