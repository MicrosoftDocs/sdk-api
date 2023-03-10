---
UID: NF:mmc.IStringTable.DeleteAllStrings
title: IStringTable::DeleteAllStrings (mmc.h)
description: The IStringTable::DeleteAllStrings method enables a snap-in to delete all strings from the snap-in's string table.
helpviewer_keywords: ["DeleteAllStrings","DeleteAllStrings method [MMC]","DeleteAllStrings method [MMC]","IStringTable interface","IStringTable interface [MMC]","DeleteAllStrings method","IStringTable.DeleteAllStrings","IStringTable::DeleteAllStrings","_slate_istringtable_deleteallstrings","mmc.istringtable_deleteallstrings","mmc/IStringTable::DeleteAllStrings"]
old-location: mmc\istringtable_deleteallstrings.htm
tech.root: mmc
ms.assetid: 9a0b02f6-3c15-4687-a1b8-2beba40dd1dc
ms.date: 12/05/2018
ms.keywords: DeleteAllStrings, DeleteAllStrings method [MMC], DeleteAllStrings method [MMC],IStringTable interface, IStringTable interface [MMC],DeleteAllStrings method, IStringTable.DeleteAllStrings, IStringTable::DeleteAllStrings, _slate_istringtable_deleteallstrings, mmc.istringtable_deleteallstrings, mmc/IStringTable::DeleteAllStrings
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
 - IStringTable::DeleteAllStrings
 - mmc/IStringTable::DeleteAllStrings
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
 - IStringTable.DeleteAllStrings
---

# IStringTable::DeleteAllStrings


## -description

The <b>IStringTable::DeleteAllStrings</b> method enables a snap-in to delete all strings from the snap-in's string table.



## -returns

This method can return one of these values.

## -remarks

This method deletes all strings from the snap-in's string table, regardless of each string's reference count.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-istringtable">IStringTable</a>



<a href="/windows/desktop/api/mmc/nf-mmc-istringtable-addstring">IStringTable::AddString</a>



<a href="/windows/desktop/api/mmc/nf-mmc-istringtable-deletestring">IStringTable::DeleteString</a>
