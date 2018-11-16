---
UID: NF:searchapi.IUrlAccessor.GetDocFormat
title: IUrlAccessor::GetDocFormat
author: windows-sdk-content
description: Gets the document format, represented as a Multipurpose Internet Mail Extensions (MIME) string.
old-location: search\_search_IUrlAccessor_GetDocFormat.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\protocolhandlers\iurlaccessor\getdocformat.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetDocFormat, GetDocFormat method [search], GetDocFormat method [search],IUrlAccessor interface, IUrlAccessor interface [search],GetDocFormat method, IUrlAccessor.GetDocFormat, IUrlAccessor::GetDocFormat, _search_IUrlAccessor_GetDocFormat, search._search_IUrlAccessor_GetDocFormat, searchapi/IUrlAccessor::GetDocFormat
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Searchapi.h
api_name:
 - IUrlAccessor.GetDocFormat
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
- apiref
: 
- COM
: 
- searchapi.h
: 
- IUrlAccessor.GetDocFormat
: 
---

# IUrlAccessor::GetDocFormat


## -description


Gets the document format, represented as a Multipurpose Internet Mail Extensions (MIME) string.
        


## -parameters




### -param wszDocFormat [out]

Type: <b>WCHAR[]</b>

Receives a pointer to a null-terminated Unicode string containing the MIME type for the current item.
                


### -param dwSize [in]

Type: <b>DWORD</b>

Size of <i>wszDocFormat</i>in <b>TCHAR</b><b>s</b>.
                


### -param pdwLength [out]

Type: <b>DWORD*</b>

Receives a pointer to the number of <b>TCHAR</b><b>s</b> written to <i>wszDocFormat</i>, not including the terminating <b>NULL</b>.
                


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The <i>wszDocFormat</i> is used to identify the correct <a href="https://msdn.microsoft.com/80b86ea0-d9d1-4d1f-b80f-90851e5bdf11">IFilter</a> for the stream returned by <a href="https://msdn.microsoft.com/02dc13c0-01a4-416d-ba14-c0390b4c4aae">IUrlAccessor::BindToStream</a>. Implement this method when the URL item is supposed to have a different association than is indicated by the file name extension or content type. For example, if .doc items are not associated with Microsoft Word, this method should return the <a href="_com_CLSID_Key">CLSID Key</a> key of the appropriate document source.

If you do not provide an implementation of this method or the <a href="https://msdn.microsoft.com/dc56bacc-17a9-450f-a57c-22a90bde24b8">IUrlAccessor::GetCLSID</a> method, the filter host uses the out parameters from <a href="https://msdn.microsoft.com/410be931-d458-458a-b0cd-4e9f0c444423">IUrlAccessor::GetFileName</a> to determine the Multipurpose Internet Mail Extensions (MIME) content type. 
            



