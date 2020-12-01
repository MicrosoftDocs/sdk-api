---
UID: NF:mmc.IStringTable.DeleteString
title: IStringTable::DeleteString (mmc.h)
description: Enables a snap-in to delete a specified string from the snap-in string table.
helpviewer_keywords: ["DeleteString","DeleteString method [MMC]","DeleteString method [MMC]","IStringTable interface","IStringTable interface [MMC]","DeleteString method","IStringTable.DeleteString","IStringTable::DeleteString","_slate_istringtable_deletestring","mmc.istringtable_deletestring","mmc/IStringTable::DeleteString"]
old-location: mmc\istringtable_deletestring.htm
tech.root: mmc
ms.assetid: 57d04890-5dd8-45e5-9b46-b982ea3a4f36
ms.date: 12/05/2018
ms.keywords: DeleteString, DeleteString method [MMC], DeleteString method [MMC],IStringTable interface, IStringTable interface [MMC],DeleteString method, IStringTable.DeleteString, IStringTable::DeleteString, _slate_istringtable_deletestring, mmc.istringtable_deletestring, mmc/IStringTable::DeleteString
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
 - IStringTable::DeleteString
 - mmc/IStringTable::DeleteString
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
 - IStringTable.DeleteString
---

# IStringTable::DeleteString


## -description

The <b>IStringTable::DeleteString</b> method enables a snap-in to delete a specified string from the snap-in string table.

## -parameters

### -param StringID [in]

The string to be deleted from the snap-in string table.

## -returns

This method can return one of these values.

## -remarks

Strings in the string table are reference counted. For example, adding the string "My Text" to the string table will return an ID, such as 1234. Adding "My Text" to the string table a second time will return an ID of 1234 again, and the internal reference count for the string will be incremented. Two calls to <b>IStringTable::DeleteString</b> will be required to completely remove "My Text" from the snap-in string table.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-istringtable">IStringTable</a>



<a href="/windows/desktop/api/mmc/nf-mmc-istringtable-addstring">IStringTable::AddString</a>



<a href="/windows/desktop/api/mmc/nf-mmc-istringtable-deleteallstrings">IStringTable::DeleteAllStrings</a>