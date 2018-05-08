---
UID: NF:dsparse.DsIsMangledRdnValueW
title: DsIsMangledRdnValueW function
author: windows-driver-content
description: Determines if a given relative distinguished name value is a mangled name of the given type.
old-location: ad\dsismangledrdnvalue.htm
old-project: AD
ms.assetid: adf5e133-9e48-4e97-af0c-4f8ea9b8bf8f
ms.author: windowsdriverdev
ms.date: 5/1/2018
ms.keywords: DsIsMangledRdnValue, DsIsMangledRdnValue function [Active Directory], DsIsMangledRdnValueA, DsIsMangledRdnValueW, _glines_dsismangledrdnvalue, ad.dsismangledrdnvalue, dsparse/DsIsMangledRdnValue, dsparse/DsIsMangledRdnValueA, dsparse/DsIsMangledRdnValueW
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
req.unicode-ansi: DsIsMangledRdnValueW (Unicode) and DsIsMangledRdnValueA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DS_MANGLE_FOR
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Ntdsapi.dll
api_name:
-	DsIsMangledRdnValue
-	DsIsMangledRdnValueA
-	DsIsMangledRdnValueW
product: Windows
targetos: Windows
req.lib: Ntdsapi.lib
req.dll: Ntdsapi.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# DsIsMangledRdnValueW function


## -description


The <b>DsIsMangledRdnValue</b> function determines if a given relative distinguished name value is a mangled name of the given type.


## -parameters




### -param pszRdn [in]

Pointer to a null-terminated string that contains  the relative distinguished name  to determine if it is mangled. The <i>cRdn</i> parameter contains the number of characters in this string.


### -param cRdn [in]

Contains the number of characters in the <i>pszRdn</i> string.


### -param eDsMangleForDesired [in]

Contains one of the <a href="https://msdn.microsoft.com/79a66a54-889e-464e-8199-ad911ea84a86">DS_MANGLE_FOR</a> values that specifies the type of name mangling to search for.


## -returns



Returns <b>TRUE</b> if the  relative distinguished name is mangled and the mangle type is the same as specified. Returns <b>FALSE</b> if the relative distinguished name is not mangled or the  mangle type is different than specified.




## -remarks



This function determines if the given relative distinguished name value is mangled and mangled in the given type.  The <i>pszRdn</i> parameter should only contain the value of the relative distinguished name and not the key.  The relative distinguished name value may be quoted or unquoted.




## -see-also




<a href="https://msdn.microsoft.com/79a66a54-889e-464e-8199-ad911ea84a86">DS_MANGLE_FOR</a>



<a href="https://msdn.microsoft.com/a92783c2-ffb8-473e-8484-1c05ca5453ff">Domain Controller and Replication Management Functions</a>



<a href="https://msdn.microsoft.com/e4aaa83c-3bd6-48db-9d34-367b76ba629c">DsIsMangledDn</a>
 

 

