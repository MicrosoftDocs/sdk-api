---
UID: NE:dsparse._DS_MANGLE_FOR
title: "_DS_MANGLE_FOR"
author: windows-sdk-content
description: The DS_MANGLE_FOR enumeration is used to define whether a relative distinguished name is mangled (encoded) and in what form the mangling occurs.
old-location: ad\ds_mangle_for.htm
tech.root: ad
ms.assetid: 79a66a54-889e-464e-8199-ad911ea84a86
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: DS_MANGLE_FOR, DS_MANGLE_FOR enumeration [Active Directory], DS_MANGLE_OBJECT_RDN_FOR_DELETION, DS_MANGLE_OBJECT_RDN_FOR_NAME_CONFLICT, DS_MANGLE_UNKNOWN, _DS_MANGLE_FOR, _glines_ds_mangle_for, ad.ds__mangle__for, ad.ds_mangle_for, dsparse/DS_MANGLE_FOR, dsparse/DS_MANGLE_OBJECT_RDN_FOR_DELETION, dsparse/DS_MANGLE_OBJECT_RDN_FOR_NAME_CONFLICT, dsparse/DS_MANGLE_UNKNOWN
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: dsparse.h
req.include-header: Ntdsapi.h
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dsparse.h
api_name:
 - DS_MANGLE_FOR
product: Windows
targetos: Windows
req.typenames: DS_MANGLE_FOR
req.redist: 
---

# _DS_MANGLE_FOR enumeration


## -description


The <b>DS_MANGLE_FOR</b> enumeration is used to define whether a 
   relative distinguished name is mangled (encoded) and in what form the mangling occurs.


## -enum-fields




### -field DS_MANGLE_UNKNOWN

Indicates that the relative distinguished name is  not mangled or that the type of mangling is 
      unknown.


### -field DS_MANGLE_OBJECT_RDN_FOR_DELETION

Indicates that the relative distinguished name has been mangled for deletion.


### -field DS_MANGLE_OBJECT_RDN_FOR_NAME_CONFLICT

Indicates that the relative distinguished name has been mangled due to a naming conflict.


## -see-also




<a href="https://msdn.microsoft.com/30711d2d-f541-46b4-a301-a0f9fc7d6676">DsCrackUnquotedMangledRdn</a>



<a href="https://msdn.microsoft.com/e4aaa83c-3bd6-48db-9d34-367b76ba629c">DsIsMangledDn</a>



<a href="https://msdn.microsoft.com/adf5e133-9e48-4e97-af0c-4f8ea9b8bf8f">DsIsMangledRdnValue</a>



<a href="https://msdn.microsoft.com/eafa3285-4474-4077-a6ad-b37f8211e7e6">Enumerations in Active Directory Domain Services</a>
 

 

