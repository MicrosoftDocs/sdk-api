---
UID: NF:shldisp.IShellFolderViewDual2.SelectItemRelative
title: IShellFolderViewDual2::SelectItemRelative (shldisp.h)
description: Selects an item relative to the current item.
helpviewer_keywords: ["IShellFolderViewDual2 interface [Windows Shell]","SelectItemRelative method","IShellFolderViewDual2.SelectItemRelative","IShellFolderViewDual2::SelectItemRelative","SelectItemRelative","SelectItemRelative method [Windows Shell]","SelectItemRelative method [Windows Shell]","IShellFolderViewDual2 interface","_shell_IShellFolderViewDual2_SelectItemRelative","shell.IShellFolderViewDual2_SelectItemRelative","shldisp/IShellFolderViewDual2::SelectItemRelative"]
old-location: shell\IShellFolderViewDual2_SelectItemRelative.htm
tech.root: shell
ms.assetid: 421a039e-49d6-4a93-958a-48c7e847fa6b
ms.date: 12/05/2018
ms.keywords: IShellFolderViewDual2 interface [Windows Shell],SelectItemRelative method, IShellFolderViewDual2.SelectItemRelative, IShellFolderViewDual2::SelectItemRelative, SelectItemRelative, SelectItemRelative method [Windows Shell], SelectItemRelative method [Windows Shell],IShellFolderViewDual2 interface, _shell_IShellFolderViewDual2_SelectItemRelative, shell.IShellFolderViewDual2_SelectItemRelative, shldisp/IShellFolderViewDual2::SelectItemRelative
req.header: shldisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shldisp.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellFolderViewDual2::SelectItemRelative
 - shldisp/IShellFolderViewDual2::SelectItemRelative
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shldisp.h
api_name:
 - IShellFolderViewDual2.SelectItemRelative
---

# IShellFolderViewDual2::SelectItemRelative


## -description

Selects an item relative to the current item.

## -parameters

### -param iRelative [in]

Type: <b>int</b>

The offset of the item to be selected in relation to the current item.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The current item is defined as the item in the view with the SVSI_SELECTIONMARK state. If there is no item with SVSI_SELECTIONMARK, the method returns S_FALSE and does nothing.

