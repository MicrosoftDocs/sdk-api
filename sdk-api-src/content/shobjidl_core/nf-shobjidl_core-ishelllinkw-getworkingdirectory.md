---
UID: NF:shobjidl_core.IShellLinkW.GetWorkingDirectory
title: IShellLinkW::GetWorkingDirectory (shobjidl_core.h)
description: Gets the name of the working directory for a Shell link object.
helpviewer_keywords: ["GetWorkingDirectory","GetWorkingDirectory method [Windows Shell]","GetWorkingDirectory method [Windows Shell]","IShellLink interface","GetWorkingDirectory method [Windows Shell]","IShellLinkA interface","GetWorkingDirectory method [Windows Shell]","IShellLinkW interface","IShellLink interface [Windows Shell]","GetWorkingDirectory method","IShellLink::GetWorkingDirectory","IShellLinkA interface [Windows Shell]","GetWorkingDirectory method","IShellLinkA::GetWorkingDirectory","IShellLinkW interface [Windows Shell]","GetWorkingDirectory method","IShellLinkW.GetWorkingDirectory","IShellLinkW::GetWorkingDirectory","_win32_IShellLink_GetWorkingDirectory","shell.IShellLink_GetWorkingDirectory","shobjidl_core/IShellLink::GetWorkingDirectory","shobjidl_core/IShellLinkA::GetWorkingDirectory","shobjidl_core/IShellLinkW::GetWorkingDirectory"]
old-location: shell\IShellLink_GetWorkingDirectory.htm
tech.root: shell
ms.assetid: cae6b2fd-362b-43a2-b0cb-b42bd103f359
ms.date: 12/05/2018
ms.keywords: GetWorkingDirectory, GetWorkingDirectory method [Windows Shell], GetWorkingDirectory method [Windows Shell],IShellLink interface, GetWorkingDirectory method [Windows Shell],IShellLinkA interface, GetWorkingDirectory method [Windows Shell],IShellLinkW interface, IShellLink interface [Windows Shell],GetWorkingDirectory method, IShellLink::GetWorkingDirectory, IShellLinkA interface [Windows Shell],GetWorkingDirectory method, IShellLinkA::GetWorkingDirectory, IShellLinkW interface [Windows Shell],GetWorkingDirectory method, IShellLinkW.GetWorkingDirectory, IShellLinkW::GetWorkingDirectory, _win32_IShellLink_GetWorkingDirectory, shell.IShellLink_GetWorkingDirectory, shobjidl_core/IShellLink::GetWorkingDirectory, shobjidl_core/IShellLinkA::GetWorkingDirectory, shobjidl_core/IShellLinkW::GetWorkingDirectory
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
 - IShellLinkW::GetWorkingDirectory
 - shobjidl_core/IShellLinkW::GetWorkingDirectory
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
 - IShellLink.GetWorkingDirectory
 - IShellLinkA.GetWorkingDirectory
 - IShellLinkW.GetWorkingDirectory
---

# IShellLinkW::GetWorkingDirectory


## -description

Gets the name of the working directory for a Shell link object.

## -parameters

### -param pszDir

Type: <b>LPTSTR</b>

The address of a buffer that receives the name of the working directory.

### -param cch

Type: <b>int</b>

The maximum number of characters to copy to the buffer pointed to by the <i>pszDir</i> parameter. The name of the working directory is truncated if it is longer than the maximum specified by this parameter.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.

