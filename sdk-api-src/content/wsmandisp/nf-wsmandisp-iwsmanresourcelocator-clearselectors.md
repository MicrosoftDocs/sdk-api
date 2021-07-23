---
UID: NF:wsmandisp.IWSManResourceLocator.ClearSelectors
title: IWSManResourceLocator::ClearSelectors (wsmandisp.h)
description: Removes all the selectors from a ResourceLocator object. You can provide a ResourceLocator object instead of specifying a resource URI in IWSManSession object operations such as Get, Put, or Enumerate.
helpviewer_keywords: ["ClearSelectors","ClearSelectors method [Windows Remote Management]","ClearSelectors method [Windows Remote Management]","IWSManResourceLocator interface","IWSManResourceLocator interface [Windows Remote Management]","ClearSelectors method","IWSManResourceLocator.ClearSelectors","IWSManResourceLocator::ClearSelectors","winrm.iwsmanresourcelocator_clearselectors","wsmandisp/IWSManResourceLocator::ClearSelectors"]
old-location: winrm\iwsmanresourcelocator_clearselectors.htm
tech.root: winrm
ms.assetid: fccd0cd4-465b-454c-a300-ab50c25d6afe
ms.date: 12/05/2018
ms.keywords: ClearSelectors, ClearSelectors method [Windows Remote Management], ClearSelectors method [Windows Remote Management],IWSManResourceLocator interface, IWSManResourceLocator interface [Windows Remote Management],ClearSelectors method, IWSManResourceLocator.ClearSelectors, IWSManResourceLocator::ClearSelectors, winrm.iwsmanresourcelocator_clearselectors, wsmandisp/IWSManResourceLocator::ClearSelectors
req.header: wsmandisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WSManDisp.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: WSManDisp.tlb
req.dll: WSMAuto.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWSManResourceLocator::ClearSelectors
 - wsmandisp/IWSManResourceLocator::ClearSelectors
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WSMAuto.dll
api_name:
 - IWSManResourceLocator.ClearSelectors
---

# IWSManResourceLocator::ClearSelectors


## -description

Removes all the <a href="/windows/desktop/WinRM/windows-remote-management-glossary">selectors</a> from a <a href="/windows/desktop/WinRM/resourcelocator">ResourceLocator</a> object. You can provide a <a href="/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsmanresourcelocator">ResourceLocator</a> object instead of specifying a resource URI in <a href="/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsmansession">IWSManSession</a> object operations such as <a href="/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmansession-get">Get</a>, <a href="/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmansession-put">Put</a>, or <a href="/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmansession-enumerate">Enumerate</a>.



## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsmanresourcelocator">IWSManResourceLocator</a>
