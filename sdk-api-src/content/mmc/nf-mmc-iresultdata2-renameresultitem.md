---
UID: NF:mmc.IResultData2.RenameResultItem
title: IResultData2::RenameResultItem (mmc.h)
description: The RenameResultItem method programmatically places the specified result item into rename mode, after which, the user can manually enter the new name.
helpviewer_keywords: ["IResultData2 interface [MMC]","RenameResultItem method","IResultData2.RenameResultItem","IResultData2::RenameResultItem","RenameResultItem","RenameResultItem method [MMC]","RenameResultItem method [MMC]","IResultData2 interface","_slate_iresultdata2_renameresultitem","mmc.iresultdata2_renameresultitem","mmc/IResultData2::RenameResultItem"]
old-location: mmc\iresultdata2_renameresultitem.htm
tech.root: mmc
ms.assetid: a667f638-88bb-4758-8df7-478b0d6c18c4
ms.date: 12/05/2018
ms.keywords: IResultData2 interface [MMC],RenameResultItem method, IResultData2.RenameResultItem, IResultData2::RenameResultItem, RenameResultItem, RenameResultItem method [MMC], RenameResultItem method [MMC],IResultData2 interface, _slate_iresultdata2_renameresultitem, mmc.iresultdata2_renameresultitem, mmc/IResultData2::RenameResultItem
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
req.lib: Mmc.lib
req.dll: Mmcndmgr.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IResultData2::RenameResultItem
 - mmc/IResultData2::RenameResultItem
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
 - IResultData2.RenameResultItem
---

# IResultData2::RenameResultItem


## -description

The 
<b>RenameResultItem</b> method programmatically places the specified result item into rename mode, after which, the user can manually enter the new name. This method is designed specifically for the case where an item is created and immediately must be placed into rename mode. Use of this method under other scenarios, such as being called after an item has been selected, is not supported and may have unexpected results.

## -parameters

### -param itemID [in]

The result item being placed into rename mode. When applied to virtual lists, pass the item index instead of the result item.

## -returns

If successful, the return value is S_OK; otherwise, the return value is an error code.  The <a href="/windows/desktop/api/winerror/nf-winerror-succeeded">SUCCEEDED</a> and/or <a href="/windows/desktop/api/winerror/nf-winerror-failed">FAILED</a> macros can be used to evaluate the return value. If the Rename verb is not enabled, this method returns E_FAIL.

## -remarks

The item being placed into rename mode must have the Rename verb enabled for this method to succeed.

## -see-also

<a href="/windows/desktop/api/mmc/nf-mmc-iconsole3-renamescopeitem">IConsole3::RenameScopeItem</a>