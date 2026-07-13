---
UID: NF:ntquery.LocateCatalogsA
title: LocateCatalogsA function (ntquery.h)
description: Finds the catalog that indexes a directory.
helpviewer_keywords: ["LocateCatalogsA", "ntquery/LocateCatalogsA"]
old-location: indexsrv\locatecatalogs.htm
tech.root: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixrefint_4t6b.htm
ms.date: 12/05/2018
ms.keywords: LocateCatalogs, LocateCatalogs function [Indexing Service], LocateCatalogsA, LocateCatalogsW, _idxs_LocateCatalogs, indexsrv.locatecatalogs, ntquery/LocateCatalogs, ntquery/LocateCatalogsA, ntquery/LocateCatalogsW
f1_keywords:
- ntquery/LocateCatalogs
dev_langs:
- c++
req.header: ntquery.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: LocateCatalogsW (Unicode) and LocateCatalogsA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ntquery.lib
req.dll: Ntquery.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Ntquery.dll
api_name:
- LocateCatalogs
- LocateCatalogsA
- LocateCatalogsW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# LocateCatalogsA function


## -description


> [!Note]  
> Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use [Windows Search](/windows/desktop/search/-search-3x-wds-overview) for client side search and [Microsoft Search Server Express](https://www.microsoft.com/download/details.aspx?id=18914) for server side search.

Finds the catalog that indexes a directory.


## -parameters




### -param pwszScope [in]

A pointer to a null-terminated string that specifies the scope for an Indexing Service query. The scope can be local (C:\directory) or a remote universal naming convention (UNC) (\\COMPUTER\SHARE\directory). The scope cannot be a redirected drive letter (a drive letter that refers to a drive on a remote computer). For Web catalogs, scopes must be physical, not IIS virtual scopes. To specify any catalog on the computer, use L"\". 


### -param iBmk [in]

The zero-based bookmark of the result to be retrieved. Pass zero to retrieve the first computer and catalog that index <i>pwszScope</i>, pass one to retrieve the second computer and catalog that index <i>pwszScope</i>, and so on. If no index for the bookmark is available, <b>LocateCatalogs</b> returns S_FALSE. 


### -param pwszMachine [out]

A Pointer to a buffer where a null-terminated string is written if the function is successful. The result string is the name of the computer on which a query over the scope <i>pwszScope</i> can be executed.


### -param pccMachine [in, out]

On input, a pointer to a character count that specifies the size of <i>pwszMachine</i>, including the terminating null character. On output, specifies the count of characters used in <i>pwszMachine</i> if the function is successful, or the count of characters needed to store the name of the computer if the buffer is too small. If the buffer is too small, <b>LocateCatalogs</b> returns S_OK.


### -param pwszCat [out]

A pointer to a buffer where a null-terminated string is written if the function is successful. The result string is the name of the catalog on which a query over the scope <i>pwszScope</i> can be executed.


### -param pccCat [in, out]

On input, a pointer to a character count that specifies the size of <i>pwszCat</i>, including the terminating null character. On output, specifies the count of characters used in <i>pwszCat</i> if the function is successful, or the count of characters needed to store the name of the catalog if the buffer is too small. If the buffer is too small, <b>LocateCatalogs</b> returns S_OK. 


## -returns



This function can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The operation was completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
No computer  and catalog can be found that index the scope, or <i>iBmk</i> is beyond the count of computers and catalogs that index the scope.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The function received an invalid parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>QUERY_E_INVALID_DIRECTORY</b></dt>
</dl>
</td>
<td width="60%">
The function received an invalid scope.

</td>
</tr>
</table>
 




## -remarks



Use the <b>LocateCatalogs</b> function to determine catalogs that cover a specific scope. If the computer and catalog are known, it's more efficient to execute a query without calling the <b>LocateCatalogs</b> function.



The <b>LocateCatalogs</b> function does not verify that the computer and catalog returned are available. If an application fails to issue a query with the computer and catalog returned, it should increment <i>iBmk</i> and call <b>LocateCatalogs</b> again to get the next computer and catalog that index the specified scope.

If a computer-and-catalog match is found but the computer and catalog buffers are not large enough, <b>LocateCatalogs</b> returns S_OK, and fills the <i>pcCat</i> and <i>pcMachine</i> parameters with the wide character count required. Callers of <b>LocateCatalogs</b> must check the return code, <i>pcMachine</i>, and <i>pcCat</i> to determine whether the call was successful. 



<div class="alert"><b>Note</b>  If <b>LocateCatalogs</b> finds a catalog that includes the path in <i>pwszScope</i>, it does not determine whether the scope is excluded for that catalog.</div>
<div> </div>

#### Examples

This example enumerates all computers and catalogs capable of resolving queries over the scope "C:\directory".




```cpp
HRESULT hr = S_OK;
 
for ( ULONG iBmk = 0; S_OK == hr; iBmk++ )
{
    TCHAR awcMachine[ MAX_COMPUTERNAME_LENGTH + 1 ];
    const ULONG cwcMachineBuffer = sizeof awcMachine / sizeof TCHAR;
    ULONG cwcMachine = cwcMachineBuffer;
    TCHAR awcCatalog[ MAX_PATH + 1 ];
    const ULONG cwcCatalogBuffer = sizeof awcCatalog / sizeof TCHAR;
    ULONG cwcCatalog = cwcCatalogBuffer;
 
    hr = LocateCatalogs( L"c:\\directory",
                         iBmk,
                         awcMachine,
                         &cwcMachine,
                         awcCatalog,
                         &cwcCatalog );
    if ( ( hr == S_OK ) &&
         ( cwcMachine <= cwcMachineBuffer ) &&
         ( cwcCatalog <= cwcCatalogBuffer ) )
    {
        wprintf( L"matching machine and catalog: '%s', '%s'\n", 
                awcMachine, awcCatalog );
    }
}
```





## -see-also




<a href="/windows/desktop/api/ntquery/nf-ntquery-setcatalogstate">SetCatalogState</a>
 

 
