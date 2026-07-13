---
UID: NN:fhcfg.IFhScopeIterator
title: IFhScopeIterator (fhcfg.h)
description: The IFhScopeIterator interface allows client applications to enumerate individual items in an inclusion or exclusion list. To retrieve inclusion and exclusion lists, call the IFhConfigMgr::GetIncludeExcludeRules method.
helpviewer_keywords: ["IFhScopeIterator","IFhScopeIterator interface [Windows API]","IFhScopeIterator interface [Windows API]","described","fhcfg/IFhScopeIterator","winprog.ifhscopeiterator"]
old-location: winprog\ifhscopeiterator.htm
tech.root: winprog
ms.assetid: E8F993BD-CB53-474A-926D-AED0F5A17073
ms.date: 12/05/2018
ms.keywords: IFhScopeIterator, IFhScopeIterator interface [Windows API], IFhScopeIterator interface [Windows API],described, fhcfg/IFhScopeIterator, winprog.ifhscopeiterator
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
 - IFhScopeIterator
 - fhcfg/IFhScopeIterator
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
 - IFhScopeIterator
---

# IFhScopeIterator interface


## -description

The <b>IFhScopeIterator</b> interface allows client applications to enumerate individual items in an inclusion or exclusion list. To retrieve inclusion and exclusion lists, call  the <a href="/windows/desktop/api/fhcfg/nf-fhcfg-ifhconfigmgr-getincludeexcluderules">IFhConfigMgr::GetIncludeExcludeRules</a> method.

> [!NOTE] 
> **IFhScopeIterator** is deprecated and may be altered or unavailable in future releases.

## -inheritance

The <b>IFhScopeIterator</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IFhScopeIterator</b> also has these types of members:

