---
UID: NF:searchapi.IUrlAccessor.GetSecurityDescriptor
title: IUrlAccessor::GetSecurityDescriptor (searchapi.h)
description: Gets the security descriptor for the URL item. Security is applied at query time, so this descriptor identifies security for read access.
helpviewer_keywords: ["GetSecurityDescriptor","GetSecurityDescriptor method [search]","GetSecurityDescriptor method [search]","IUrlAccessor interface","IUrlAccessor interface [search]","GetSecurityDescriptor method","IUrlAccessor.GetSecurityDescriptor","IUrlAccessor::GetSecurityDescriptor","_search_IUrlAccessor_GetSecurityDescriptor","search._search_IUrlAccessor_GetSecurityDescriptor","searchapi/IUrlAccessor::GetSecurityDescriptor"]
old-location: search\_search_IUrlAccessor_GetSecurityDescriptor.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\protocolhandlers\iurlaccessor\getsecuritydescriptor.htm
ms.date: 12/05/2018
ms.keywords: GetSecurityDescriptor, GetSecurityDescriptor method [search], GetSecurityDescriptor method [search],IUrlAccessor interface, IUrlAccessor interface [search],GetSecurityDescriptor method, IUrlAccessor.GetSecurityDescriptor, IUrlAccessor::GetSecurityDescriptor, _search_IUrlAccessor_GetSecurityDescriptor, search._search_IUrlAccessor_GetSecurityDescriptor, searchapi/IUrlAccessor::GetSecurityDescriptor
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
 - IUrlAccessor::GetSecurityDescriptor
 - searchapi/IUrlAccessor::GetSecurityDescriptor
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
 - IUrlAccessor.GetSecurityDescriptor
---

# IUrlAccessor::GetSecurityDescriptor


## -description

Gets the security descriptor for the URL item. Security is applied at query time, so this descriptor identifies security for read access.

## -parameters

### -param pSD [out]

Type: <b>BYTE*</b>

Receives a pointer to the security descriptor.

### -param dwSize [in]

Type: <b>DWORD</b>

Size in <b>TCHAR</b><b>s</b> of the <i>pSD</i> array.

### -param pdwLength [out]

Type: <b>DWORD*</b>

Receives a pointer to the number of <b>TCHAR</b><b>s</b> written to <i>pSD</i>, not including the terminating <b>NULL</b>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method allows custom mappings between users registered to a content source and those users registered on the domain, if they are different. Security descriptors created in this method must be self-relative.
            

If the URL contains a user security identifier (SID), then the protocol handler is invoked in the security context of that user, and this method must return E_NOTIMPL. 
            

If the URL does not contain a user SID, then the protocol handler is invoked in the security context of the system service. In that case, this method can return either an access control list (ACL) to restrict read access, or <a href="/windows/desktop/search/-search-prth-error-constants">PRTH_S_ACL_IS_READ_EVERYONE</a> to allow anyone read access during querying.
            

<div class="alert"><b>Note</b>  If this method returns E_NOTIMPL and the URL does NOT contain a user SID, then the item is retrievable by all user queries.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor">IUrlAccessor</a>



<a href="/windows/desktop/search/-search-prth-error-constants">Search Protocol Handler Error Messages</a>