---
UID: NF:shobjidl_core.IShellLinkW.SetWorkingDirectory
title: IShellLinkW::SetWorkingDirectory (shobjidl_core.h)
description: Sets the name of the working directory for a Shell link object. (Unicode)
helpviewer_keywords: ["IShellLink interface [Windows Shell]","SetWorkingDirectory method","IShellLink::SetWorkingDirectory","IShellLinkA","IShellLinkA interface [Windows Shell]","SetWorkingDirectory method","IShellLinkA::SetWorkingDirectory","IShellLinkW","IShellLinkW interface [Windows Shell]","SetWorkingDirectory method","IShellLinkW.SetWorkingDirectory","IShellLinkW::SetWorkingDirectory","SetWorkingDirectory","SetWorkingDirectory method [Windows Shell]","SetWorkingDirectory method [Windows Shell]","IShellLink interface","SetWorkingDirectory method [Windows Shell]","IShellLinkA interface","SetWorkingDirectory method [Windows Shell]","IShellLinkW interface","_win32_IShellLink_SetWorkingDirectory","shell.IShellLink_SetWorkingDirectory","shobjidl_core/IShellLink::SetWorkingDirectory","shobjidl_core/IShellLinkA::SetWorkingDirectory","shobjidl_core/IShellLinkW::SetWorkingDirectory"]
old-location: shell\IShellLink_SetWorkingDirectory.htm
tech.root: shell
ms.assetid: 03767add-766c-4970-935e-ffa5aa401a95
ms.date: 12/05/2018
ms.keywords: IShellLink interface [Windows Shell],SetWorkingDirectory method, IShellLink::SetWorkingDirectory, IShellLinkA, IShellLinkA interface [Windows Shell],SetWorkingDirectory method, IShellLinkA::SetWorkingDirectory, IShellLinkW, IShellLinkW interface [Windows Shell],SetWorkingDirectory method, IShellLinkW.SetWorkingDirectory, IShellLinkW::SetWorkingDirectory, SetWorkingDirectory, SetWorkingDirectory method [Windows Shell], SetWorkingDirectory method [Windows Shell],IShellLink interface, SetWorkingDirectory method [Windows Shell],IShellLinkA interface, SetWorkingDirectory method [Windows Shell],IShellLinkW interface, _win32_IShellLink_SetWorkingDirectory, shell.IShellLink_SetWorkingDirectory, shobjidl_core/IShellLink::SetWorkingDirectory, shobjidl_core/IShellLinkA::SetWorkingDirectory, shobjidl_core/IShellLinkW::SetWorkingDirectory
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
 - IShellLinkW::SetWorkingDirectory
 - shobjidl_core/IShellLinkW::SetWorkingDirectory
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
 - IShellLink.SetWorkingDirectory
 - IShellLinkA.SetWorkingDirectory
 - IShellLinkW.SetWorkingDirectory
---

# IShellLinkW::SetWorkingDirectory


## -description

Sets the name of the working directory for a Shell link object.

## -parameters

### -param pszDir

Type: <b>LPCTSTR</b>

The address of a buffer that contains the name of the new working directory.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The working directory is optional unless the target requires a working directory. For example, if an application creates a Shell link to a Microsoft Word document that uses a template residing in a different directory, the application would use this method to set the working directory.

