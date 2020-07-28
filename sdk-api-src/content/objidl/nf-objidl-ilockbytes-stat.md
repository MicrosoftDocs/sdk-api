---
UID: NF:objidl.ILockBytes.Stat
title: ILockBytes::Stat (objidl.h)
description: The Stat method retrieves a STATSTG structure containing information for this byte array object.
helpviewer_keywords: ["ILockBytes interface [Structured Storage]","Stat method","ILockBytes.Stat","ILockBytes::Stat","Stat","Stat method [Structured Storage]","Stat method [Structured Storage]","ILockBytes interface","_stg_ilockbytes_stat","objidl/ILockBytes::Stat","stg.ilockbytes_stat"]
old-location: stg\ilockbytes_stat.htm
tech.root: Stg
ms.assetid: e7953f21-ac34-44e3-9b6f-b93ac89e2e32
ms.date: 12/05/2018
ms.keywords: ILockBytes interface [Structured Storage],Stat method, ILockBytes.Stat, ILockBytes::Stat, Stat, Stat method [Structured Storage], Stat method [Structured Storage],ILockBytes interface, _stg_ilockbytes_stat, objidl/ILockBytes::Stat, stg.ilockbytes_stat
f1_keywords:
- objidl/ILockBytes.Stat
dev_langs:
- c++
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Objidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Ole32.dll
api_name:
- ILockBytes.Stat
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ILockBytes::Stat


## -description


The <b>Stat</b> method retrieves a 
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/ns-objidl-statstg">STATSTG</a> structure containing information for this byte array object.


## -parameters




### -param pstatstg [out]

Pointer to a 
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/ns-objidl-statstg">STATSTG</a> structure in which this method places information about this byte array object. The pointer is <b>NULL</b> if an error occurs.


### -param grfStatFlag [in]

Specifies whether this method should supply the <b>pwcsName</b> member of the 
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/ns-objidl-statstg">STATSTG</a> structure through values taken from the 
<a href="https://docs.microsoft.com/windows/desktop/api/wtypes/ne-wtypes-statflag">STATFLAG</a> enumeration. If the STATFLAG_NONAME is specified, the <b>pwcsName</b> member of 
<b>STATSTG</b> is not supplied, thus saving a memory-allocation operation. The other possible value, STATFLAG_DEFAULT, indicates that all members of the 
<b>STATSTG</b> structure be supplied.


## -returns



This method can return one of these values.




## -remarks



<b>ILockBytes::Stat</b> should supply information about the byte array object in a 
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/ns-objidl-statstg">STATSTG</a> structure.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Stg/ilockbytes-file-based-implementation">ILockBytes - File-Based Implementation</a>



<a href="https://docs.microsoft.com/windows/desktop/Stg/ilockbytes-global-memory-implementation">ILockBytes - Global Memory Implementation</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wtypes/ne-wtypes-statflag">STATFLAG</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objidl/ns-objidl-statstg">STATSTG</a>
 

 

