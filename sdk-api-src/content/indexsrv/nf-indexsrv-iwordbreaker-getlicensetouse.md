---
UID: NF:indexsrv.IWordBreaker.GetLicenseToUse
title: IWordBreaker::GetLicenseToUse (indexsrv.h)
description: Gets a pointer to the license information for this implementation of the IWordBreaker interface.
helpviewer_keywords: ["GetLicenseToUse","GetLicenseToUse method [search]","GetLicenseToUse method [search]","IWordBreaker interface","IWordBreaker interface [search]","GetLicenseToUse method","IWordBreaker.GetLicenseToUse","IWordBreaker::GetLicenseToUse","_search_IWordBreaker_GetLicenseToUse","indexsrv/IWordBreaker::GetLicenseToUse","search._search_IWordBreaker_GetLicenseToUse"]
old-location: search\_search_IWordBreaker_GetLicenseToUse.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\dataaddins\iwordbreaker\getlicensetouse.htm
ms.date: 12/05/2018
ms.keywords: GetLicenseToUse, GetLicenseToUse method [search], GetLicenseToUse method [search],IWordBreaker interface, IWordBreaker interface [search],GetLicenseToUse method, IWordBreaker.GetLicenseToUse, IWordBreaker::GetLicenseToUse, _search_IWordBreaker_GetLicenseToUse, indexsrv/IWordBreaker::GetLicenseToUse, search._search_IWordBreaker_GetLicenseToUse
req.header: indexsrv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows NT 4.0 Option Pack
ms.custom: 19H1
f1_keywords:
 - IWordBreaker::GetLicenseToUse
 - indexsrv/IWordBreaker::GetLicenseToUse
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Indexsrv.h
api_name:
 - IWordBreaker.GetLicenseToUse
---

# IWordBreaker::GetLicenseToUse


## -description

Gets a pointer to the license information for this implementation of the <a href="/windows/desktop/api/indexsrv/nn-indexsrv-iwordbreaker">IWordBreaker</a> interface.

## -parameters

### -param ppwcsLicense [out]

Type: <b>WCHAR const**</b>

Pointer to a variable that receives a pointer to the license information for this <a href="/windows/desktop/api/indexsrv/nn-indexsrv-iwordbreaker">IWordBreaker</a> implementation.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.