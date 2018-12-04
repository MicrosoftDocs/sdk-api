---
UID: NF:shobjidl_core.IShellLinkW.SetWorkingDirectory
title: IShellLinkW::SetWorkingDirectory
author: windows-sdk-content
description: Sets the name of the working directory for a Shell link object.
old-location: shell\IShellLink_SetWorkingDirectory.htm
tech.root: shell
ms.assetid: 03767add-766c-4970-935e-ffa5aa401a95
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: IShellLink interface [Windows Shell],SetWorkingDirectory method, IShellLink::SetWorkingDirectory, IShellLinkA, IShellLinkA interface [Windows Shell],SetWorkingDirectory method, IShellLinkA::SetWorkingDirectory, IShellLinkW, IShellLinkW interface [Windows Shell],SetWorkingDirectory method, IShellLinkW.SetWorkingDirectory, IShellLinkW::SetWorkingDirectory, SetWorkingDirectory, SetWorkingDirectory method [Windows Shell], SetWorkingDirectory method [Windows Shell],IShellLink interface, SetWorkingDirectory method [Windows Shell],IShellLinkA interface, SetWorkingDirectory method [Windows Shell],IShellLinkW interface, _win32_IShellLink_SetWorkingDirectory, shell.IShellLink_SetWorkingDirectory, shobjidl_core/IShellLink::SetWorkingDirectory, shobjidl_core/IShellLinkA::SetWorkingDirectory, shobjidl_core/IShellLinkW::SetWorkingDirectory
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The working directory is optional unless the target requires a working directory. For example, if an application creates a Shell link to a Microsoft Word document that uses a template residing in a different directory, the application would use this method to set the working directory.



