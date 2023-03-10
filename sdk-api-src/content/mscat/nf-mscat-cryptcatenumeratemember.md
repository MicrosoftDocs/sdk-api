---
UID: NF:mscat.CryptCATEnumerateMember
title: CryptCATEnumerateMember function (mscat.h)
description: Enumerates the members of a catalog.
helpviewer_keywords: ["CryptCATEnumerateMember","CryptCATEnumerateMember function [Security]","mscat/CryptCATEnumerateMember","security.cryptcatenumeratemember"]
old-location: security\cryptcatenumeratemember.htm
tech.root: security
ms.assetid: 6bbfef11-a150-4255-8620-27c1b1587b48
ms.date: 12/05/2018
ms.keywords: CryptCATEnumerateMember, CryptCATEnumerateMember function [Security], mscat/CryptCATEnumerateMember, security.cryptcatenumeratemember
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
 - CryptCATEnumerateMember
 - mscat/CryptCATEnumerateMember
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wintrust.dll
api_name:
 - CryptCATEnumerateMember
---

# CryptCATEnumerateMember function


## -description

<p class="CCE_Message">[The <b>CryptCATEnumerateMember</b> function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CryptCATEnumerateMember</b> function enumerates the members of a catalog.

## -parameters

### -param hCatalog [in]

The handle of the catalog that contains the members to enumerate. This value cannot be <b>NULL</b>.

### -param pPrevMember [in]

A pointer to a [CRYPTCATMEMBER](/windows/desktop/api/mscat/ns-mscat-cryptcatmember) structure that identifies which member of the catalog was last retrieved. If this parameter is <b>NULL</b>, this function will retrieve the first member of the catalog.

## -returns

This function returns a pointer to a [CRYPTCATMEMBER](/windows/desktop/api/mscat/ns-mscat-cryptcatmember) structure that represents the next member of the catalog. If there are no more members in the catalog to enumerate, this function returns <b>NULL</b>.

## -remarks

Do not free the returned pointer nor any of the members pointed to by the returned pointer.


#### Examples

The following pseudocode example shows how to use this function to enumerate all of the members of a catalog.


```cpp
CRYPTCATMEMBER *pMember = NULL;

for(pMember = CryptCATEnumerateMember(hCatalog, pMember); 
    NULL != pMember; 
    pMember = CryptCATEnumerateMember(hCatalog, pMember))
{
   // Use the catalog member.
}
```

## -see-also

[CRYPTCATMEMBER](/windows/desktop/api/mscat/ns-mscat-cryptcatmember)