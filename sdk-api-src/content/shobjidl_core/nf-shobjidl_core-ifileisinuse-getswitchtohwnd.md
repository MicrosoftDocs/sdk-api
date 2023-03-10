---
UID: NF:shobjidl_core.IFileIsInUse.GetSwitchToHWND
title: IFileIsInUse::GetSwitchToHWND (shobjidl_core.h)
description: Retrieves the handle of the top-level window of the application that is using the file.
helpviewer_keywords: ["GetSwitchToHWND","GetSwitchToHWND method [Windows Shell]","GetSwitchToHWND method [Windows Shell]","IFileIsInUse interface","IFileIsInUse interface [Windows Shell]","GetSwitchToHWND method","IFileIsInUse.GetSwitchToHWND","IFileIsInUse::GetSwitchToHWND","_shell_IFileIsInUse_GetSwitchToHWND","shell.IFileIsInUse_GetSwitchToHWND","shobjidl_core/IFileIsInUse::GetSwitchToHWND"]
old-location: shell\IFileIsInUse_GetSwitchToHWND.htm
tech.root: shell
ms.assetid: b4223cb0-2027-4073-9558-99ae27f4e52a
ms.date: 12/05/2018
ms.keywords: GetSwitchToHWND, GetSwitchToHWND method [Windows Shell], GetSwitchToHWND method [Windows Shell],IFileIsInUse interface, IFileIsInUse interface [Windows Shell],GetSwitchToHWND method, IFileIsInUse.GetSwitchToHWND, IFileIsInUse::GetSwitchToHWND, _shell_IFileIsInUse_GetSwitchToHWND, shell.IFileIsInUse_GetSwitchToHWND, shobjidl_core/IFileIsInUse::GetSwitchToHWND
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
 - IFileIsInUse::GetSwitchToHWND
 - shobjidl_core/IFileIsInUse::GetSwitchToHWND
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
 - IFileIsInUse.GetSwitchToHWND
---

# IFileIsInUse::GetSwitchToHWND


## -description

Retrieves the handle of the top-level window of the application that is using the file.

## -parameters

### -param phwnd [out]

Type: <b>HWND*</b>

A pointer to an <b>HWND</b> value that, when this method returns successfully, receives the window handle.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Only files that return the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileisinuse-getcapabilities">capability flag</a> OF_CAP_CANSWITCHTO can be switched to.