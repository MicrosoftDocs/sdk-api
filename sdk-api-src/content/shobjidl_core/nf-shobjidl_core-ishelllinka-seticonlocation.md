---
UID: NF:shobjidl_core.IShellLinkA.SetIconLocation
title: IShellLinkA::SetIconLocation (shobjidl_core.h)
description: Sets the location (path and index) of the icon for a Shell link object. (ANSI)
helpviewer_keywords: ["IShellLink interface [Windows Shell]","SetIconLocation method","IShellLink::SetIconLocation","IShellLinkA interface [Windows Shell]","SetIconLocation method","IShellLinkA.SetIconLocation","IShellLinkA::SetIconLocation","IShellLinkW interface [Windows Shell]","SetIconLocation method","IShellLinkW::SetIconLocation","SetIconLocation","SetIconLocation method [Windows Shell]","SetIconLocation method [Windows Shell]","IShellLink interface","SetIconLocation method [Windows Shell]","IShellLinkA interface","SetIconLocation method [Windows Shell]","IShellLinkW interface","_win32_IShellLink_SetIconLocation","shell.IShellLink_SetIconLocation","shobjidl_core/IShellLink::SetIconLocation","shobjidl_core/IShellLinkA::SetIconLocation","shobjidl_core/IShellLinkW::SetIconLocation"]
old-location: shell\IShellLink_SetIconLocation.htm
tech.root: shell
ms.assetid: 1ba267f2-ae05-4a6d-be3c-382a89e17d92
ms.date: 12/05/2018
ms.keywords: IShellLink interface [Windows Shell],SetIconLocation method, IShellLink::SetIconLocation, IShellLinkA interface [Windows Shell],SetIconLocation method, IShellLinkA.SetIconLocation, IShellLinkA::SetIconLocation, IShellLinkW interface [Windows Shell],SetIconLocation method, IShellLinkW::SetIconLocation, SetIconLocation, SetIconLocation method [Windows Shell], SetIconLocation method [Windows Shell],IShellLink interface, SetIconLocation method [Windows Shell],IShellLinkA interface, SetIconLocation method [Windows Shell],IShellLinkW interface, _win32_IShellLink_SetIconLocation, shell.IShellLink_SetIconLocation, shobjidl_core/IShellLink::SetIconLocation, shobjidl_core/IShellLinkA::SetIconLocation, shobjidl_core/IShellLinkW::SetIconLocation
req.header: shobjidl_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellLinkA::SetIconLocation
 - shobjidl_core/IShellLinkA::SetIconLocation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellLink.SetIconLocation
 - IShellLinkA.SetIconLocation
 - IShellLinkW.SetIconLocation
---

# IShellLinkA::SetIconLocation


## -description

Sets the location (path and index) of the icon for a Shell link object.

## -parameters

### -param pszIconPath

Type: <b>LPCTSTR</b>

The address of a buffer to contain the path of the file containing the icon.

### -param iIcon

Type: <b>int</b>

The index of the icon.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

