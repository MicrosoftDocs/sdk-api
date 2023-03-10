---
UID: NF:mmc.IStringTable.Enumerate
title: IStringTable::Enumerate (mmc.h)
description: Supplies a pointer to an IEnumString interface on an enumerator that can return the strings in a snap-in's string table.
helpviewer_keywords: ["Enumerate","Enumerate method [MMC]","Enumerate method [MMC]","IStringTable interface","IStringTable interface [MMC]","Enumerate method","IStringTable.Enumerate","IStringTable::Enumerate","_slate_istringtable_enumerate","mmc.istringtable_enumerate","mmc/IStringTable::Enumerate"]
old-location: mmc\istringtable_enumerate.htm
tech.root: mmc
ms.assetid: 3d23e29d-a80f-4710-8285-c9e64fd580a1
ms.date: 12/05/2018
ms.keywords: Enumerate, Enumerate method [MMC], Enumerate method [MMC],IStringTable interface, IStringTable interface [MMC],Enumerate method, IStringTable.Enumerate, IStringTable::Enumerate, _slate_istringtable_enumerate, mmc.istringtable_enumerate, mmc/IStringTable::Enumerate
req.header: mmc.h
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
req.dll: Mmcndmgr.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IStringTable::Enumerate
 - mmc/IStringTable::Enumerate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmcndmgr.dll
api_name:
 - IStringTable.Enumerate
---

# IStringTable::Enumerate


## -description

The <b>IStringTable::Enumerate</b> method supplies a pointer to an <a href="/windows/desktop/api/objidl/nn-objidl-ienumstring">IEnumString</a> interface on an enumerator that can return the strings in a snap-in's string table. The <a href="/windows/desktop/api/objidl/nn-objidl-ienumstring">IEnumString</a> interface is a standard COM interface.

## -parameters

### -param ppEnum [out]

The address of <a href="/windows/desktop/api/objidl/nn-objidl-ienumstring">IEnumString</a>* pointer variable that receives the interface pointer to the enumerator. If an error occurs, *<i>ppEnum</i> is set to <b>NULL</b>. If *<i>ppEnum </i> is non-<b>NULL</b>, MMC's implementation of <b>IEnumString</b> calls <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">IUnknown::AddRef</a> on the *<i>ppEnum</i>. The snap-in must call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> when the interface is no longer required.

## -returns

This method can return one of these values.

## -remarks

The returned <a href="/windows/desktop/api/objidl/nn-objidl-ienumstring">IEnumString</a> enumeration represents a snapshot of the collection of strings in the underlying string table the time that the enumeration was retrieved. Neither <a href="/windows/desktop/api/objidl/nf-objidl-ienumstring-reset">IEnumString::Reset</a>, nor IEnumString::Clone takes a new snapshot of the collection.

The implementation of <a href="/windows/desktop/api/objidl/nn-objidl-ienumstring">IEnumString</a> uses the default OLE task memory allocator to allocate memory for the strings it returns.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-istringtable">IStringTable</a>



<a href="/windows/desktop/api/mmc/nf-mmc-istringtable-findstring">IStringTable::FindString</a>