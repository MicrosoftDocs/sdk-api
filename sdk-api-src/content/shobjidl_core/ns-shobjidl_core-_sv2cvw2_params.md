---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a>*</b>

A <b>RECT</b> structure that defines the view's display area.


### -field pvid

Type: <b>const SHELLVIEWID*</b>

A pointer to a view ID. The view ID can be one of the Windows-defined VIDs or a custom, view-defined VID. This value takes precedence over the view mode designated in the <a href="https://msdn.microsoft.com/be00fe39-1add-412e-b88b-4b0b1404b19d">FOLDERSETTINGS</a> structure pointed to by <b>pfs</b>.


### -field hwndView

Type: <b>HWND</b>

A window handle to the new Shell view.

