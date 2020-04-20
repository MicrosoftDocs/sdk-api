---
UID: NF:objidl.IStorage.Stat
title: IStorage::Stat (objidl.h)
description: The Stat method retrieves the STATSTG structure for this open storage object.helpviewer_keywords: ["IStorage interface [Structured Storage]","Stat method","IStorage.Stat","IStorage::Stat","Stat","Stat method [Structured Storage]","Stat method [Structured Storage]","IStorage interface","_stg_istorage_stat","objidl/IStorage::Stat","stg.istorage_stat"]
old-location: stg\istorage_stat.htm
tech.root: Stg
ms.assetid: 87478fa8-1b5f-44ed-bffc-e139c7f44a12
ms.date: 12/05/2018
ms.keywords: IStorage interface [Structured Storage],Stat method, IStorage.Stat, IStorage::Stat, Stat, Stat method [Structured Storage], Stat method [Structured Storage],IStorage interface, _stg_istorage_stat, objidl/IStorage::Stat, stg.istorage_stat
f1_keywords:
- objidl/IStorage.Stat
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
- IStorage.Stat
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IStorage::Stat


## -description


The <b>Stat</b> method retrieves the 
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/ns-objidl-statstg">STATSTG</a> structure for this open storage object.


## -parameters




### -param pstatstg [out]

On return, pointer to a 
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/ns-objidl-statstg">STATSTG</a> structure where this method places information about the open storage object. This parameter is <b>NULL</b> if an error occurs.


### -param grfStatFlag [in]

Specifies that some of the members in the 
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/ns-objidl-statstg">STATSTG</a> structure are not returned, thus saving a memory allocation operation. Values are taken from the 
<a href="https://docs.microsoft.com/windows/desktop/api/wtypes/ne-wtypes-statflag">STATFLAG</a> enumeration.


## -returns



This method can return one of these values.




## -remarks



<b>IStorage::Stat</b> retrieves the 
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/ns-objidl-statstg">STATSTG</a> structure for the current storage object. The 
<b>STATSTG</b> structure contains statistical information about the storage object. <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-istorage-enumelements">IStorage::EnumElements</a> returns a pointer to an enumerator object. The enumerator object returned by this method implements the 
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-ienumstatstg">IEnumSTATSTG</a> interface, through which the data stored in the array of the 
<b>STATSTG</b> structures is enumerated.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-ienumstatstg">IEnumSTATSTG</a>



<a href="https://docs.microsoft.com/windows/desktop/Stg/istorage-compound-file-implementation">IStorage - Compound File Implementation</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-istorage-setclass">IStorage::SetClass</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-istorage-setelementtimes">IStorage::SetElementTimes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-istorage-setstatebits">IStorage::SetStateBits</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wtypes/ne-wtypes-statflag">STATFLAG</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objidl/ns-objidl-statstg">STATSTG</a>
 

 

