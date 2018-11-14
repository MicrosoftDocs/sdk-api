---
UID: NF:shobjidl_core.IFileIsInUse.GetSwitchToHWND
title: IFileIsInUse::GetSwitchToHWND
author: windows-sdk-content
description: Retrieves the handle of the top-level window of the application that is using the file.
old-location: shell\IFileIsInUse_GetSwitchToHWND.htm
tech.root: shell
ms.assetid: b4223cb0-2027-4073-9558-99ae27f4e52a
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GetSwitchToHWND, GetSwitchToHWND method [Windows Shell], GetSwitchToHWND method [Windows Shell],IFileIsInUse interface, IFileIsInUse interface [Windows Shell],GetSwitchToHWND method, IFileIsInUse.GetSwitchToHWND, IFileIsInUse::GetSwitchToHWND, _shell_IFileIsInUse_GetSwitchToHWND, shell.IFileIsInUse_GetSwitchToHWND, shobjidl_core/IFileIsInUse::GetSwitchToHWND
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IFileIsInUse.GetSwitchToHWND
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- shobjidl_core.h
: 
- IFileIsInUse.GetSwitchToHWND
: 
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

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Only files that return the <a href="https://msdn.microsoft.com/d2ce674a-4c06-401d-bfb0-bc2a086ef89c">capability flag</a> OF_CAP_CANSWITCHTO can be switched to.



