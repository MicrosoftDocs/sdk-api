---
UID: NF:shlobj.IShellFolderBand.InitializeSFB
title: IShellFolderBand::InitializeSFB
author: windows-sdk-content
description: Initializes an IShellFolderBand object.
old-location: shell\IShellFolderBand_InitializeSFB.htm
tech.root: shell
ms.assetid: 2f0582d2-b079-4b97-8da0-211b6ef1b8f3
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: IShellFolderBand interface [Windows Shell],InitializeSFB method, IShellFolderBand.InitializeSFB, IShellFolderBand::InitializeSFB, InitializeSFB, InitializeSFB method [Windows Shell], InitializeSFB method [Windows Shell],IShellFolderBand interface, _win32_IShellFolderBand_InitializeSFB, shell.IShellFolderBand_InitializeSFB, shlobj/IShellFolderBand::InitializeSFB
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shlobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shlobj.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll (version 5.00 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellFolderBand.InitializeSFB
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellFolderBand::InitializeSFB


## -description


Initializes an <a href="https://msdn.microsoft.com/88ae35ea-6ff9-431c-848b-84fc61d3c690">IShellFolderBand</a> object.


## -parameters




### -param psf

Type: <b><a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a> object.


### -param pidl

Type: <b>PCIDLIST_ABSOLUTE</b>

A PIDL.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a>



<a href="https://msdn.microsoft.com/88ae35ea-6ff9-431c-848b-84fc61d3c690">IShellFolderBand</a>
 

 

