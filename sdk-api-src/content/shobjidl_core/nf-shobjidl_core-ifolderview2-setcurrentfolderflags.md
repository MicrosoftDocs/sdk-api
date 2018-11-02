---
UID: NF:shobjidl_core.IFolderView2.SetCurrentFolderFlags
title: IFolderView2::SetCurrentFolderFlags
author: windows-sdk-content
description: Sets and applies specified folder flags.
old-location: shell\IFolderView2_SetCurrentFolderFlags.htm
tech.root: shell
ms.assetid: 94999ac7-c9dd-439e-8f63-eeb226763200
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IFolderView2 interface [Windows Shell],SetCurrentFolderFlags method, IFolderView2.SetCurrentFolderFlags, IFolderView2::SetCurrentFolderFlags, SetCurrentFolderFlags, SetCurrentFolderFlags method [Windows Shell], SetCurrentFolderFlags method [Windows Shell],IFolderView2 interface, _shell_IFolderView2_SetCurrentFolderFlags, shell.IFolderView2_SetCurrentFolderFlags, shobjidl_core/IFolderView2::SetCurrentFolderFlags
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IFolderView2.SetCurrentFolderFlags
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFolderView2::SetCurrentFolderFlags


## -description


Sets and applies specified folder flags.


## -parameters




### -param dwMask [in]

Type: <b>DWORD</b>

The value of type <b>DWORD</b> that specifies the bitmask indicating which items in the structure are desired or valid.


### -param dwFlags [in]

Type: <b>DWORD</b>

The value of type <b>DWORD</b> that contains one or more <a href="https://msdn.microsoft.com/e471b81a-da4d-48c0-8c7f-996b507d27a1">FOLDERFLAGS</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<b>For Windows 7 or later:</b> This method must be used in combinaton with the <i>FVO_CUSTOMPOSITION</i> flag from the <a href="https://msdn.microsoft.com/ab0ebc82-e917-4e3a-864b-fc3bb6280a48">FOLDERVIEWOPTIONS</a> enumeration.



