---
UID: NF:mscat.CryptCATAdminEnumCatalogFromHash
title: CryptCATAdminEnumCatalogFromHash function (mscat.h)
description: Enumerates the catalogs that contain a specified hash.
helpviewer_keywords: ["CryptCATAdminEnumCatalogFromHash","CryptCATAdminEnumCatalogFromHash function [Security]","mscat/CryptCATAdminEnumCatalogFromHash","security.cryptcatadminenumcatalogfromhash"]
old-location: security\cryptcatadminenumcatalogfromhash.htm
tech.root: security
ms.assetid: 33ab2d01-94ab-4d23-a054-9da0731485d6
ms.date: 12/05/2018
ms.keywords: CryptCATAdminEnumCatalogFromHash, CryptCATAdminEnumCatalogFromHash function [Security], mscat/CryptCATAdminEnumCatalogFromHash, security.cryptcatadminenumcatalogfromhash
req.header: mscat.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wintrust.lib
req.dll: Wintrust.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CryptCATAdminEnumCatalogFromHash
 - mscat/CryptCATAdminEnumCatalogFromHash
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wintrust.dll
 - mscat32.dll
api_name:
 - CryptCATAdminEnumCatalogFromHash
---

# CryptCATAdminEnumCatalogFromHash function


## -description


<p class="CCE_Message">[The  <b>CryptCATAdminEnumCatalogFromHash</b> function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]


The <b>CryptCATAdminEnumCatalogFromHash</b> function enumerates the catalogs that contain a specified hash. The hash is typically returned from the <a href="https://docs.microsoft.com/windows/desktop/api/mscat/nf-mscat-cryptcatadmincalchashfromfilehandle">CryptCATAdminCalcHashFromFileHandle</a> function. After the final call to this function, call <a href="https://docs.microsoft.com/windows/desktop/api/mscat/nf-mscat-cryptcatadminreleasecatalogcontext">CryptCATAdminReleaseCatalogContext</a> to release allocated memory.



## -parameters




### -param hCatAdmin [in]

A handle to a catalog administrator context previously assigned by the <a href="/windows/desktop/api/mscat/nf-mscat-cryptcatadminacquirecontext">CryptCATAdminAcquireContext</a> function.


### -param pbHash [in]

A pointer to the buffer that contains the hash retrieved by calling <a href="/windows/desktop/api/mscat/nf-mscat-cryptcatadmincalchashfromfilehandle">CryptCATAdminCalcHashFromFileHandle</a>.


### -param cbHash [in]

Number of bytes in the buffer allocated for <i>pbHash</i>.


### -param dwFlags [in]

This parameter is reserved for future use and must be set to zero.


### -param phPrevCatInfo [in]

A pointer to the handle to the previous catalog context or <b>NULL</b>. To get the first catalog that contains the hash, or to start an enumeration of all catalogs, pass <b>NULL</b> for this parameter. To continue the enumeration, pass the previous call's return value until no more catalogs are found.


## -returns




The return value is a handle to the catalog context, or <b>NULL</b> if there are no more catalogs to enumerate. 
  
**Note:** The type HCATINFO is simply a typedef for HANDLE, which makes it easy to accidentally use the HCATINFO in the wrong context. In particular, this is NOT the same as a HANDLE returned from **CryptCATOpen**, even though the compiler will not prevent you from using the HCATINFO in any function that expects a catalog handle. To acquire a catalog handle from this function, first call [**CryptCATCatalogInfoFromContext**](/windows/win32/api/mscat/nf-mscat-cryptcatcataloginfofromcontext) to get the filename of the catalog, and then call [**CryptCATOpen**](/windows/win32/api/mscat/nf-mscat-cryptcatopen) with that filename.
  
 


For extended error information, call the <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function. For a complete list of error codes provided by the operating system, see <a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">System Error Codes</a>.



**Note:** The function returns a value of type **HCATINFO**, but this is simply a typedef for **HANDLE**. Because of this, it is easy to accidentally use the **HCATINFO** when calling a function that expects a different kind of **HANDLE**. In particular, this is not the same as a **HANDLE** returned from **CryptCATOpen**, even though the compiler will not prevent you from using the **HCATINFO** in any function that expects a catalog handle. 
  
To acquire a catalog handle from this function, first call [CryptCATCatalogInfoFromContext](/windows/win32/api/mscat/nf-mscat-cryptcatcataloginfofromcontext) to get the filename of the catalog, and then call [CryptCATOpen](/windows/win32/api/mscat/nf-mscat-cryptcatopen) with that filename to open the catalog.

