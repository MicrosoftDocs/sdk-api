---
UID: NF:shobjidl.IFolderViewOptions.GetFolderViewOptions
title: IFolderViewOptions::GetFolderViewOptions
author: windows-sdk-content
description: Retrieves the current set of options for the view.
old-location: shell\IFolderViewOptions_GetFolderViewOptions.htm
tech.root: shell
ms.assetid: 9733c2b0-608f-4f20-b379-81de0c333473
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: GetFolderViewOptions, GetFolderViewOptions method [Windows Shell], GetFolderViewOptions method [Windows Shell],IFolderViewOptions interface, IFolderViewOptions interface [Windows Shell],GetFolderViewOptions method, IFolderViewOptions.GetFolderViewOptions, IFolderViewOptions::GetFolderViewOptions, _shell_IFolderViewOptions_GetFolderViewOptions, shell.IFolderViewOptions_GetFolderViewOptions, shobjidl/IFolderViewOptions::GetFolderViewOptions
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
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
req.dll: ExplorerFrame.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ExplorerFrame.dll
api_name:
 - IFolderViewOptions.GetFolderViewOptions
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFolderViewOptions::GetFolderViewOptions


## -description


Retrieves the current set of options for the view.


## -parameters




### -param pfvoFlags [out]

Type: <b><a href="https://msdn.microsoft.com/ab0ebc82-e917-4e3a-864b-fc3bb6280a48">FOLDERVIEWOPTIONS</a>*</b>

A bitmask that, when this method returns successfully, receives the <a href="https://msdn.microsoft.com/ab0ebc82-e917-4e3a-864b-fc3bb6280a48">FOLDERVIEWOPTIONS</a> values that are currently set.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



