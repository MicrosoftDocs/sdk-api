---
UID: NF:shobjidl_core.IEnumShellItems.Skip
title: IEnumShellItems::Skip (shobjidl_core.h)
description: Skips a given number of IShellItem interfaces in the enumeration. Used when retrieving interfaces.
helpviewer_keywords: ["IEnumShellItems interface [Windows Shell]","Skip method","IEnumShellItems.Skip","IEnumShellItems::Skip","Skip","Skip method [Windows Shell]","Skip method [Windows Shell]","IEnumShellItems interface","_shell_IEnumShellItems_Skip","shell.IEnumShellItems_Skip","shobjidl_core/IEnumShellItems::Skip"]
old-location: shell\IEnumShellItems_Skip.htm
tech.root: shell
ms.assetid: 5359c9d2-715a-4949-8f40-a35d04423dba
ms.date: 12/05/2018
ms.keywords: IEnumShellItems interface [Windows Shell],Skip method, IEnumShellItems.Skip, IEnumShellItems::Skip, Skip, Skip method [Windows Shell], Skip method [Windows Shell],IEnumShellItems interface, _shell_IEnumShellItems_Skip, shell.IEnumShellItems_Skip, shobjidl_core/IEnumShellItems::Skip
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
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
 - IEnumShellItems::Skip
 - shobjidl_core/IEnumShellItems::Skip
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IEnumShellItems.Skip
---

# IEnumShellItems::Skip


## -description

Skips a given number of <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> interfaces in the enumeration. Used when retrieving interfaces.

## -parameters

### -param celt [in]

Type: <b>ULONG</b>

The number of <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> interfaces to skip.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumshellitems">IEnumShellItems</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>