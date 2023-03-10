---
UID: NF:mmc.IStringTable.AddString
title: IStringTable::AddString (mmc.h)
description: Enables a snap-in to add a string to the snap-in's string table.
helpviewer_keywords: ["AddString","AddString method [MMC]","AddString method [MMC]","IStringTable interface","IStringTable interface [MMC]","AddString method","IStringTable.AddString","IStringTable::AddString","_slate_istringtable_addstring","mmc.istringtable_addstring","mmc/IStringTable::AddString"]
old-location: mmc\istringtable_addstring.htm
tech.root: mmc
ms.assetid: fd4672fb-89d1-4542-b917-58c01290c928
ms.date: 12/05/2018
ms.keywords: AddString, AddString method [MMC], AddString method [MMC],IStringTable interface, IStringTable interface [MMC],AddString method, IStringTable.AddString, IStringTable::AddString, _slate_istringtable_addstring, mmc.istringtable_addstring, mmc/IStringTable::AddString
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
 - IStringTable::AddString
 - mmc/IStringTable::AddString
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
 - IStringTable.AddString
---

# IStringTable::AddString


## -description

The <b>IStringTable::AddString</b> method enables a snap-in to add a string to the snap-in's string table.

## -parameters

### -param pszAdd [in]

The string to add to the string table.

### -param pStringID [out]

A pointer to the ID of the string added to the string table.

## -returns

This method can return one of these values.

## -remarks

Strings in the string table are reference counted. For example, adding the string "My Text" to the string table will return an ID, say 1234. Adding "My Text" to the string table a second time will return an ID of 1234 again, and the internal reference count for the string will be incremented. Two calls to 
<a href="/windows/desktop/api/mmc/nf-mmc-istringtable-deletestring">IStringTable::DeleteString</a>, or a single call to 
<a href="/windows/desktop/api/mmc/nf-mmc-istringtable-deleteallstrings">IStringTable::DeleteAllStrings</a>, will be required to completely remove "My Text" from the snap-in's string table.

<b>IStringTable::AddString</b> returns a nonzero string ID if the call to it was successful. Snap-ins therefore can safely use 0 to indicate an unassigned ID.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-istringtable">IStringTable</a>



<a href="/windows/desktop/api/mmc/nf-mmc-istringtable-deleteallstrings">IStringTable::DeleteAllStrings</a>



<a href="/windows/desktop/api/mmc/nf-mmc-istringtable-deletestring">IStringTable::DeleteString</a>