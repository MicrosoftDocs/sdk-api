---
UID: NF:dsparse.DsCrackUnquotedMangledRdnA
title: DsCrackUnquotedMangledRdnA function
author: windows-sdk-content
description: The DsCrackUnquotedMangledRdn function unmangles (unencodes) a given relative distinguished name and returns both the decoded GUID and the mangling type used.
old-location: ad\dscrackunquotedmangledrdn.htm
tech.root: ad
ms.assetid: 30711d2d-f541-46b4-a301-a0f9fc7d6676
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: DsCrackUnquotedMangledRdn, DsCrackUnquotedMangledRdn function [Active Directory], DsCrackUnquotedMangledRdnA, DsCrackUnquotedMangledRdnW, _glines_dscrackunquotedmangledrdn, ad.dscrackunquotedmangledrdn, dsparse/DsCrackUnquotedMangledRdn, dsparse/DsCrackUnquotedMangledRdnA, dsparse/DsCrackUnquotedMangledRdnW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: dsparse.h
req.include-header: Ntdsapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DsCrackUnquotedMangledRdnW (Unicode) and DsCrackUnquotedMangledRdnA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ntdsapi.lib
req.dll: Ntdsapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ntdsapi.dll
api_name:
 - DsCrackUnquotedMangledRdn
 - DsCrackUnquotedMangledRdnA
 - DsCrackUnquotedMangledRdnW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DsCrackUnquotedMangledRdnA function


## -description


The <b>DsCrackUnquotedMangledRdn</b> function unmangles (unencodes) a given relative distinguished name and returns both the decoded GUID and the mangling type used.


## -parameters




### -param pszRDN [in]

Pointer to a string that contains the relative distinguished name (RDN) to translate. This string length is specified by the <i>cchRDN</i> parameter, so this string is not required to be null-terminated. This string must be in unquoted form. For more information about unquoted relative distinguished names, see 
<a href="https://msdn.microsoft.com/6e3dd220-ba98-46b5-8522-93cbe2029aa4">DsUnquoteRdnValue</a>.


### -param cchRDN [in]

Contains the length, in characters, of the <i>pszRDN</i> string.


### -param pGuid [out, optional]

Pointer to <b>GUID</b> value that receives the GUID of the unmangled relative distinguished name.  This parameter can be <b>NULL</b>.


### -param peDsMangleFor [out, optional]

Pointer 
to a <a href="https://msdn.microsoft.com/79a66a54-889e-464e-8199-ad911ea84a86">DS_MANGLE_FOR</a> value that receives the type of mangling used in the mangled relative distinguished name.  This parameter can be <b>NULL</b>.


## -returns



This function returns <b>TRUE</b> if the relative distinguished name is mangled or <b>FALSE</b> otherwise. If this function returns <b>FALSE</b>, neither <i>pGuid</i> or <i>peDsMangleFor</i> receive any data.




## -remarks



This function attempts to
    decode (unmangle)  an RDN that has been previously mangled due to a deletion or a naming conflict. If the relative distinguished name is mangled, the function returns <b>TRUE</b> and retrieves the GUID and mangle type, if requested.  If the relative distinguished name is not mangled, the function returns <b>FALSE</b>.




## -see-also




<a href="https://msdn.microsoft.com/79a66a54-889e-464e-8199-ad911ea84a86">DS_MANGLE_FOR</a>



<a href="https://msdn.microsoft.com/a92783c2-ffb8-473e-8484-1c05ca5453ff">Domain Controller and Replication Management Functions</a>



<a href="https://msdn.microsoft.com/e4aaa83c-3bd6-48db-9d34-367b76ba629c">DsIsMangledDn</a>



<a href="https://msdn.microsoft.com/adf5e133-9e48-4e97-af0c-4f8ea9b8bf8f">DsIsMangledRdnValue</a>



<a href="https://msdn.microsoft.com/6e3dd220-ba98-46b5-8522-93cbe2029aa4">DsUnquoteRdnValue</a>
 

 

