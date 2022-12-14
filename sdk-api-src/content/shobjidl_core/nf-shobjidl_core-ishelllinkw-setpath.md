---
UID: NF:shobjidl_core.IShellLinkW.SetPath
title: IShellLinkW::SetPath (shobjidl_core.h)
description: Sets the path and file name for the target of a Shell link object. (Unicode)
helpviewer_keywords: ["IShellLink interface [Windows Shell]","SetPath method","IShellLink::SetPath","IShellLinkA interface [Windows Shell]","SetPath method","IShellLinkA::SetPath","IShellLinkW interface [Windows Shell]","SetPath method","IShellLinkW.SetPath","IShellLinkW::SetPath","SetPath","SetPath method [Windows Shell]","SetPath method [Windows Shell]","IShellLink interface","SetPath method [Windows Shell]","IShellLinkA interface","SetPath method [Windows Shell]","IShellLinkW interface","_win32_IShellLink_SetPath","shell.IShellLink_SetPath","shobjidl_core/IShellLink::SetPath","shobjidl_core/IShellLinkA::SetPath","shobjidl_core/IShellLinkW::SetPath"]
old-location: shell\IShellLink_SetPath.htm
tech.root: shell
ms.assetid: 032610ba-d6ff-4200-8fd3-455460587dec
ms.date: 12/05/2018
ms.keywords: IShellLink interface [Windows Shell],SetPath method, IShellLink::SetPath, IShellLinkA interface [Windows Shell],SetPath method, IShellLinkA::SetPath, IShellLinkW interface [Windows Shell],SetPath method, IShellLinkW.SetPath, IShellLinkW::SetPath, SetPath, SetPath method [Windows Shell], SetPath method [Windows Shell],IShellLink interface, SetPath method [Windows Shell],IShellLinkA interface, SetPath method [Windows Shell],IShellLinkW interface, _win32_IShellLink_SetPath, shell.IShellLink_SetPath, shobjidl_core/IShellLink::SetPath, shobjidl_core/IShellLinkA::SetPath, shobjidl_core/IShellLinkW::SetPath
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
 - IShellLinkW::SetPath
 - shobjidl_core/IShellLinkW::SetPath
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
 - IShellLink.SetPath
 - IShellLinkA.SetPath
 - IShellLinkW.SetPath
---

# IShellLinkW::SetPath


## -description

Sets the path and file name for the target of a Shell link object.

## -parameters

### -param pszFile

Type: <b>LPCTSTR</b>

The address of a buffer that contains the new path.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

