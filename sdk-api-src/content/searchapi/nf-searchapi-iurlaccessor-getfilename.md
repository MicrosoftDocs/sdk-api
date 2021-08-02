---
UID: NF:searchapi.IUrlAccessor.GetFileName
title: IUrlAccessor::GetFileName (searchapi.h)
description: Retrieves the file name of the item, which the filter host uses for indexing. If the item does not exist in a file system and the IUrlAccessor::BindToStream method is implemented, this method returns the shell's System.ParsingPath property for the item.
helpviewer_keywords: ["GetFileName","GetFileName method [search]","GetFileName method [search]","IUrlAccessor interface","IUrlAccessor interface [search]","GetFileName method","IUrlAccessor.GetFileName","IUrlAccessor::GetFileName","_search_IUrlAccessor_GetFileName","search._search_IUrlAccessor_GetFileName","searchapi/IUrlAccessor::GetFileName"]
old-location: search\_search_IUrlAccessor_GetFileName.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\protocolhandlers\iurlaccessor\getfilename.htm
ms.date: 12/05/2018
ms.keywords: GetFileName, GetFileName method [search], GetFileName method [search],IUrlAccessor interface, IUrlAccessor interface [search],GetFileName method, IUrlAccessor.GetFileName, IUrlAccessor::GetFileName, _search_IUrlAccessor_GetFileName, search._search_IUrlAccessor_GetFileName, searchapi/IUrlAccessor::GetFileName
req.header: searchapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Urlaccsdk.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
f1_keywords:
 - IUrlAccessor::GetFileName
 - searchapi/IUrlAccessor::GetFileName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Searchapi.h
api_name:
 - IUrlAccessor.GetFileName
---

# IUrlAccessor::GetFileName


## -description

Retrieves the file name of the item, which the filter host uses for indexing. If the item does not exist in a file system and the <a href="/windows/desktop/api/searchapi/nf-searchapi-iurlaccessor-bindtostream">IUrlAccessor::BindToStream</a> method is implemented, this method returns the shell's System.ParsingPath property for the item.

## -parameters

### -param wszFileName [out]

Type: <b>WCHAR[]</b>

Receives the file name as a null-terminated Unicode string.

### -param dwSize [in]

Type: <b>DWORD</b>

Size in 
                <b>TCHAR</b><b>s</b> of
                <i>wszFileName</i>, not including the terminating <b>NULL</b>.

### -param pdwLength [out]

Type: <b>DWORD*</b>

Receives a pointer to the number of 
           <b>TCHAR</b><b>s</b> written to <b>wszFileName</b>, not including
                <b>NULL</b>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If this method is implemented, the filter host uses the file name to determine the correct <a href="/windows/desktop/api/filter/nn-filter-ifilter">IFilter</a> to use to parse the content of the stream returned by <a href="/windows/desktop/api/searchapi/nf-searchapi-iurlaccessor-bindtostream">IUrlAccessor::BindToStream</a>.