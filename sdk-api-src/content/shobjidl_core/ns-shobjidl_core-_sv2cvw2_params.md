---
UID: NS:shobjidl_core._SV2CVW2_PARAMS
title: "_SV2CVW2_PARAMS"
author: windows-sdk-content
description: Holds the parameters for the IShellView2::CreateViewWindow2 method.
old-location: shell\SV2CVW2_PARAMS.htm
tech.root: shell
ms.assetid: 7e165654-74ea-4d8b-81b7-11257f87af53
ms.author: windowssdkdev
ms.date: 10/17/2018
ms.keywords: "*LPSV2CVW2_PARAMS, LPSV2CVW2_PARAMS, LPSV2CVW2_PARAMS structure pointer [Windows Shell], SV2CVW2_PARAMS, SV2CVW2_PARAMS structure [Windows Shell], _SV2CVW2_PARAMS, _win32_SV2CVW2_PARAMS, shell.SV2CVW2_PARAMS, shobjidl_core/LPSV2CVW2_PARAMS, shobjidl_core/SV2CVW2_PARAMS"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shobjidl_core.h
api_name:
 - SV2CVW2_PARAMS
product: Windows
targetos: Windows
req.typenames: SV2CVW2_PARAMS, *LPSV2CVW2_PARAMS
req.redist: 
---

# _SV2CVW2_PARAMS structure


## -description


Holds the parameters for the <a href="https://msdn.microsoft.com/3b829f5f-26ea-4987-be05-6725eeff5fed">IShellView2::CreateViewWindow2</a> method.


## -struct-fields




### -field cbSize

Type: <b>DWORD</b>

The size of the structure.


### -field psvPrev

Type: <b><a href="https://msdn.microsoft.com/91438583-e4f1-456f-a130-2a45846fd725">IShellView</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/91438583-e4f1-456f-a130-2a45846fd725">IShellView</a> interface of the previous view. A Shell view can use this parameter to communicate with a previous view with the same implementation. It can also be used to optimize browsing between like views. This parameter may be <b>NULL</b>.


### -field pfs

Type: <b>LPFOLDERSETTINGS</b>

A <a href="https://msdn.microsoft.com/be00fe39-1add-412e-b88b-4b0b1404b19d">FOLDERSETTINGS</a> structure with information needed to create the view.


### -field psbOwner

Type: <b><a href="https://msdn.microsoft.com/138d90e3-a1f0-4faf-88ca-16c7a46df0ca">IShellBrowser</a>*</b>

A pointer to the current instance of the <a href="https://msdn.microsoft.com/138d90e3-a1f0-4faf-88ca-16c7a46df0ca">IShellBrowser</a> interface of the parent Shell browser. <a href="https://msdn.microsoft.com/3b829f5f-26ea-4987-be05-6725eeff5fed">IShellView2::CreateViewWindow2</a> should call this interface's <a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">AddRef</a> method and store the interface pointer. It can be used for communication with the Windows Explorer window.


### -field prcView

Type: <b><a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a>*</b>

A <b>RECT</b> structure that defines the view's display area.


### -field pvid

Type: <b>const SHELLVIEWID*</b>

A pointer to a view ID. The view ID can be one of the Windows-defined VIDs or a custom, view-defined VID. This value takes precedence over the view mode designated in the <a href="https://msdn.microsoft.com/be00fe39-1add-412e-b88b-4b0b1404b19d">FOLDERSETTINGS</a> structure pointed to by <b>pfs</b>.


### -field hwndView

Type: <b>HWND</b>

A window handle to the new Shell view.

