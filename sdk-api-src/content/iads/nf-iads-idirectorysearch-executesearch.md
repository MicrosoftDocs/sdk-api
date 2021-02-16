---
UID: NF:iads.IDirectorySearch.ExecuteSearch
title: IDirectorySearch::ExecuteSearch (iads.h)
description: The IDirectorySearch::ExecuteSearch method executes a search and passes the results to the caller.
helpviewer_keywords: ["ExecuteSearch","ExecuteSearch method [ADSI]","ExecuteSearch method [ADSI]","IDirectorySearch interface","IDirectorySearch interface [ADSI]","ExecuteSearch method","IDirectorySearch.ExecuteSearch","IDirectorySearch::ExecuteSearch","_ds_idirectorysearch_executesearch","adsi.idirectorysearch__executesearch","adsi.idirectorysearch_executesearch","iads/IDirectorySearch::ExecuteSearch"]
old-location: adsi\idirectorysearch_executesearch.htm
tech.root: adsi
ms.assetid: 7514b372-1a7a-4a42-a814-af70a727c477
ms.date: 12/05/2018
ms.keywords: ExecuteSearch, ExecuteSearch method [ADSI], ExecuteSearch method [ADSI],IDirectorySearch interface, IDirectorySearch interface [ADSI],ExecuteSearch method, IDirectorySearch.ExecuteSearch, IDirectorySearch::ExecuteSearch, _ds_idirectorysearch_executesearch, adsi.idirectorysearch__executesearch, adsi.idirectorysearch_executesearch, iads/IDirectorySearch::ExecuteSearch
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
 - IDirectorySearch::ExecuteSearch
 - iads/IDirectorySearch::ExecuteSearch
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
 - IDirectorySearch.ExecuteSearch
---

# IDirectorySearch::ExecuteSearch


## -description

The <b>IDirectorySearch::ExecuteSearch</b> method executes a search and passes the results to the caller. Some providers, such as LDAP, will defer the actual execution until the caller invokes the  <a href="/windows/desktop/api/iads/nf-iads-idirectorysearch-getfirstrow">IDirectorySearch::GetFirstRow</a> method or the  <a href="/windows/desktop/api/iads/nf-iads-idirectorysearch-getnextrow">IDirectorySearch::GetNextRow</a> method.

## -parameters

### -param pszSearchFilter [in]

A search filter string in LDAP format, such as "(objectClass=user)".

### -param pAttributeNames [in]

An array of attribute names for which data is requested. If <b>NULL</b>, <i>dwNumberAttributes</i> must be 0 or 0xFFFFFFFF.

### -param dwNumberAttributes [in]

The size of the <i>pAttributeNames</i> array. The special value 0xFFFFFFFF indicates that <i>pAttributeNames</i> is ignored and can be <b>NULL</b>.  This special value means that all attributes that are set are requested.  If this value is 0 the <i>pAttributeNames</i> array can be <b>NULL</b>.  No attribute will be requested.

### -param phSearchResult [out]

The address of a method-allocated handle to the search context. The caller passes this handle to other methods of  <a href="/windows/desktop/api/iads/nn-iads-idirectorysearch">IDirectorySearch</a> to examine the search result. If <b>NULL</b>, the search cannot be executed.

## -returns

This method returns the standard return values, as well as the following:

For more information and other return values, see  <a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>.

## -remarks

When the search filter (<i>pszSearchFilter</i>) contains an attribute of <b>ADS_UTC_TIME</b> type, it value must be of the "yymmddhhmmssZ" format where "y", "m", "d", "h", "m" and "s" stand for year, month, day, hour, minute, and second, respectively. In this format, for example, "10:20:00 May 13<sup>th</sup>, 1999" becomes "990513102000Z". The final letter "Z" is the required syntax and indicated Zulu Time or Universal Coordinated Time.

The caller must call  <a href="/windows/desktop/api/iads/nf-iads-idirectorysearch-closesearchhandle">IDirectorySearch::CloseSearchHandle</a> to release the memory allocated for the search handle and the result.

When using the special value of 0xFFFFFFFF for <i>dwNumberAttributes</i>, LDAP retrieval of ADsPath or distinguishedName has no extra resource or time cost.


#### Examples

The following C++ code example shows how to invoke  <b>IDirectorySearch::ExecuteSearch</b>.


```cpp
LPWSTR pszAttr[] = { L"ADsPath", L"Name", L"samAccountName" };
ADS_SEARCH_HANDLE hSearch;
DWORD dwCount= sizeof(pszAttr)/sizeof(LPWSTR);
 
// Search for users with a last name that begins with "h".
hr = m_pSearch->ExecuteSearch(L"(&(objectClass=user)(sn=h*))", pszAttr, dwCount, &hSearch );
```

## -see-also

<a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>



<a href="/windows/desktop/api/iads/nn-iads-idirectorysearch">IDirectorySearch</a>



<a href="/windows/desktop/api/iads/nf-iads-idirectorysearch-closesearchhandle">IDirectorySearch::CloseSearchHandle</a>



<a href="/windows/desktop/api/iads/nf-iads-idirectorysearch-getfirstrow">IDirectorySearch::GetFirstRow</a>



<a href="/windows/desktop/api/iads/nf-iads-idirectorysearch-getnextrow">IDirectorySearch::GetNextRow</a>