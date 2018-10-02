---
UID: NF:dsparse.DsIsMangledDnW
title: DsIsMangledDnW function
author: windows-sdk-content
description: The DsIsMangledDn function determines if the first relative distinguished name (RDN) in a distinguished name (DN) is a mangled name of a given type.
old-location: ad\dsismangleddn.htm
tech.root: AD
ms.assetid: e4aaa83c-3bd6-48db-9d34-367b76ba629c
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: DsIsMangledDn, DsIsMangledDn function [Active Directory], DsIsMangledDnA, DsIsMangledDnW, _glines_dsismangleddn, ad.dsismangleddn, dsparse/DsIsMangledDn, dsparse/DsIsMangledDnA, dsparse/DsIsMangledDnW
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
req.unicode-ansi: DsIsMangledDnW (Unicode) and DsIsMangledDnA (ANSI)
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
 - DsIsMangledDn
 - DsIsMangledDnA
 - DsIsMangledDnW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DsIsMangledDnW function


## -description


The <b>DsIsMangledDn</b> function determines if the first relative distinguished name (RDN) in a distinguished name (DN) is a mangled name of a given type.


## -parameters




### -param pszDn [in]

Pointer to a null-terminated string that contains the  distinguished name to retrieve the relative distinguished name from. This can also be a quoted distinguished name  as returned by other directory service functions.


### -param eDsMangleFor [in]

Contains one of the <a href="https://msdn.microsoft.com/79a66a54-889e-464e-8199-ad911ea84a86">DS_MANGLE_FOR</a> values that specifies the type of name mangling to look for.


## -returns



Returns <b>TRUE</b> if the first relative distinguished name in <i>pszDn</i> is mangled in the manner specified by <i>eDsMangleFor</i> or <b>FALSE</b>  otherwise.




## -see-also




<a href="https://msdn.microsoft.com/79a66a54-889e-464e-8199-ad911ea84a86">DS_MANGLE_FOR</a>



<a href="https://msdn.microsoft.com/a92783c2-ffb8-473e-8484-1c05ca5453ff">Domain Controller and Replication Management Functions</a>



<a href="https://msdn.microsoft.com/adf5e133-9e48-4e97-af0c-4f8ea9b8bf8f">DsIsMangledRdnValue</a>
 

 

