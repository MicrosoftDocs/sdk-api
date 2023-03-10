---
UID: NF:shobjidl_core.IFileIsInUse.GetCapabilities
title: IFileIsInUse::GetCapabilities (shobjidl_core.h)
description: Determines whether the file can be closed and whether the UI is capable of switching to the window of the application that is using the file.
helpviewer_keywords: ["GetCapabilities","GetCapabilities method [Windows Shell]","GetCapabilities method [Windows Shell]","IFileIsInUse interface","IFileIsInUse interface [Windows Shell]","GetCapabilities method","IFileIsInUse.GetCapabilities","IFileIsInUse::GetCapabilities","OF_CAP_CANCLOSE","OF_CAP_CANSWITCHTO","_shell_IFileIsInUse_GetCapabilities","shell.IFileIsInUse_GetCapabilities","shobjidl_core/IFileIsInUse::GetCapabilities"]
old-location: shell\IFileIsInUse_GetCapabilities.htm
tech.root: shell
ms.assetid: d2ce674a-4c06-401d-bfb0-bc2a086ef89c
ms.date: 12/05/2018
ms.keywords: GetCapabilities, GetCapabilities method [Windows Shell], GetCapabilities method [Windows Shell],IFileIsInUse interface, IFileIsInUse interface [Windows Shell],GetCapabilities method, IFileIsInUse.GetCapabilities, IFileIsInUse::GetCapabilities, OF_CAP_CANCLOSE, OF_CAP_CANSWITCHTO, _shell_IFileIsInUse_GetCapabilities, shell.IFileIsInUse_GetCapabilities, shobjidl_core/IFileIsInUse::GetCapabilities
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
 - IFileIsInUse::GetCapabilities
 - shobjidl_core/IFileIsInUse::GetCapabilities
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
 - IFileIsInUse.GetCapabilities
---

# IFileIsInUse::GetCapabilities


## -description

Determines whether the file can be closed and whether the UI is capable of switching to the window of the application that is using the file.

## -parameters

### -param pdwCapFlags [out]

Type: <b>DWORD*</b>

A pointer to a value that, when this method returns successfully, receives the capability flags. One or both of the following values:



#### OF_CAP_CANSWITCHTO (0x0001)

0x0001. The UI can switch to the top-level window of the application that is using the file.



#### OF_CAP_CANCLOSE (0x0002)

0x0002. The file can be closed.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The capabilities returned by this method can be used in the composition of the dialog box presented to the user that informs them of the sharing conflict. For instance, if the OF_CAP_CANSWITCHTO flag is retrieved, a button can be added to the dialog box that will switch the user to the conflicting application window (based on the <b>HWND</b> information retrieved by <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileisinuse-getswitchtohwnd">IFileIsInUse::GetSwitchToHWND</a>) so that the user can address the situation as they see fit. If the OF_CAP_CANCLOSE flag is retrieved, the dialog box can present a <b>Close</b> button that calls the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileisinuse-closefile">CloseFile</a> method.