---
UID: NF:shobjidl_core.IShellLinkW.GetIconLocation
title: IShellLinkW::GetIconLocation (shobjidl_core.h)
description: Gets the location (path and index) of the icon for a Shell link object. (Unicode)
helpviewer_keywords: ["GetIconLocation","GetIconLocation method [Windows Shell]","GetIconLocation method [Windows Shell]","IShellLink interface","GetIconLocation method [Windows Shell]","IShellLinkA interface","GetIconLocation method [Windows Shell]","IShellLinkW interface","IShellLink interface [Windows Shell]","GetIconLocation method","IShellLink::GetIconLocation","IShellLinkA interface [Windows Shell]","GetIconLocation method","IShellLinkA::GetIconLocation","IShellLinkW interface [Windows Shell]","GetIconLocation method","IShellLinkW.GetIconLocation","IShellLinkW::GetIconLocation","_win32_IShellLink_GetIconLocation","shell.IShellLink_GetIconLocation","shobjidl_core/IShellLink::GetIconLocation","shobjidl_core/IShellLinkA::GetIconLocation","shobjidl_core/IShellLinkW::GetIconLocation"]
old-location: shell\IShellLink_GetIconLocation.htm
tech.root: shell
ms.assetid: ff7cc9be-a762-472a-9846-4dbd0ec94ad1
ms.date: 12/05/2018
ms.keywords: GetIconLocation, GetIconLocation method [Windows Shell], GetIconLocation method [Windows Shell],IShellLink interface, GetIconLocation method [Windows Shell],IShellLinkA interface, GetIconLocation method [Windows Shell],IShellLinkW interface, IShellLink interface [Windows Shell],GetIconLocation method, IShellLink::GetIconLocation, IShellLinkA interface [Windows Shell],GetIconLocation method, IShellLinkA::GetIconLocation, IShellLinkW interface [Windows Shell],GetIconLocation method, IShellLinkW.GetIconLocation, IShellLinkW::GetIconLocation, _win32_IShellLink_GetIconLocation, shell.IShellLink_GetIconLocation, shobjidl_core/IShellLink::GetIconLocation, shobjidl_core/IShellLinkA::GetIconLocation, shobjidl_core/IShellLinkW::GetIconLocation
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
 - IShellLinkW::GetIconLocation
 - shobjidl_core/IShellLinkW::GetIconLocation
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
 - IShellLink.GetIconLocation
 - IShellLinkA.GetIconLocation
 - IShellLinkW.GetIconLocation
---

# IShellLinkW::GetIconLocation


## -description

Gets the location (path and index) of the icon for a Shell link object.

## -parameters

### -param pszIconPath

Type: <b>LPTSTR</b>

The address of a buffer that receives the path of the file containing the icon.

### -param cch

Type: <b>int</b>

The maximum number of characters to copy to the buffer pointed to by the <i>pszIconPath</i> parameter.

### -param piIcon

Type: <b>int*</b>

The address of a value that receives the index of the icon.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

