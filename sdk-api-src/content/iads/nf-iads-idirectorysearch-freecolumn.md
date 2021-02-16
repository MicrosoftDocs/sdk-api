---
UID: NF:iads.IDirectorySearch.FreeColumn
title: IDirectorySearch::FreeColumn (iads.h)
description: The IDirectorySearch::FreeColumn method releases memory that the IDirectorySearch::GetColumn method allocated for data for the column.
helpviewer_keywords: ["FreeColumn","FreeColumn method [ADSI]","FreeColumn method [ADSI]","IDirectorySearch interface","IDirectorySearch interface [ADSI]","FreeColumn method","IDirectorySearch.FreeColumn","IDirectorySearch::FreeColumn","_ds_idirectorysearch_freecolumn","adsi.idirectorysearch__freecolumn","adsi.idirectorysearch_freecolumn","iads/IDirectorySearch::FreeColumn"]
old-location: adsi\idirectorysearch_freecolumn.htm
tech.root: adsi
ms.assetid: 72e75429-d22c-490f-a1f7-d771628067c9
ms.date: 12/05/2018
ms.keywords: FreeColumn, FreeColumn method [ADSI], FreeColumn method [ADSI],IDirectorySearch interface, IDirectorySearch interface [ADSI],FreeColumn method, IDirectorySearch.FreeColumn, IDirectorySearch::FreeColumn, _ds_idirectorysearch_freecolumn, adsi.idirectorysearch__freecolumn, adsi.idirectorysearch_freecolumn, iads/IDirectorySearch::FreeColumn
req.header: iads.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.dll: Activeds.dll; Adsldp.dll; Adsldpc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirectorySearch::FreeColumn
 - iads/IDirectorySearch::FreeColumn
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Activeds.dll
 - Adsldp.dll
 - Adsldpc.dll
api_name:
 - IDirectorySearch.FreeColumn
---

# IDirectorySearch::FreeColumn


## -description

The <b>IDirectorySearch::FreeColumn</b> method 
    releases memory that the 
    <a href="/windows/desktop/api/iads/nf-iads-idirectorysearch-getcolumn">IDirectorySearch::GetColumn</a> method allocated 
    for data for the column.

## -parameters

### -param pSearchColumn [in]

Provides a pointer to the column to be freed.

## -returns

This method returns the standard return values, as well as the following:

For other return values, see <a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>.

## -see-also

<a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>



<a href="/windows/desktop/api/iads/nn-iads-idirectorysearch">IDirectorySearch</a>



<a href="/windows/desktop/api/iads/nf-iads-idirectorysearch-getcolumn">IDirectorySearch::GetColumn</a>