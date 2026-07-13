---
UID: NF:indexsrv.IStemmer.GetLicenseToUse
title: IStemmer::GetLicenseToUse (indexsrv.h)
description: Gets the license information for this IStemmer implementation.
helpviewer_keywords: ["GetLicenseToUse","GetLicenseToUse method [search]","GetLicenseToUse method [search]","IStemmer interface","IStemmer interface [search]","GetLicenseToUse method","IStemmer.GetLicenseToUse","IStemmer::GetLicenseToUse","_search_IStemmer_GetLicenseToUse","indexsrv/IStemmer::GetLicenseToUse","search._search_IStemmer_GetLicenseToUse"]
old-location: search\_search_IStemmer_GetLicenseToUse.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\dataaddins\istemmer\getlicensetouse.htm
ms.date: 12/05/2018
ms.keywords: GetLicenseToUse, GetLicenseToUse method [search], GetLicenseToUse method [search],IStemmer interface, IStemmer interface [search],GetLicenseToUse method, IStemmer.GetLicenseToUse, IStemmer::GetLicenseToUse, _search_IStemmer_GetLicenseToUse, indexsrv/IStemmer::GetLicenseToUse, search._search_IStemmer_GetLicenseToUse
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
 - IStemmer::GetLicenseToUse
 - indexsrv/IStemmer::GetLicenseToUse
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
 - IStemmer.GetLicenseToUse
---

# IStemmer::GetLicenseToUse


## -description

Gets the license information for this <a href="/windows/desktop/api/indexsrv/nn-indexsrv-istemmer">IStemmer</a> implementation.

## -parameters

### -param ppwcsLicense [out]

Type: <b>const WCHAR**</b>

Pointer to a variable that receives a pointer to the license information for this <a href="/windows/desktop/api/indexsrv/nn-indexsrv-istemmer">IStemmer</a> implementation.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Windows Search does not enforce license restrictions. The implementation determines the storage method for the license information.