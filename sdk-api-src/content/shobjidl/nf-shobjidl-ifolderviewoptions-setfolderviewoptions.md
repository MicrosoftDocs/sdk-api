---
UID: NF:shobjidl.IFolderViewOptions.SetFolderViewOptions
title: IFolderViewOptions::SetFolderViewOptions
author: windows-sdk-content
description: Sets specified options for the view.
old-location: shell\IFolderViewOptions_SetFolderViewOptions.htm
tech.root: Shell
ms.assetid: e170f60f-9b6c-4765-8aad-b370b08db053
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IFolderViewOptions interface [Windows Shell],SetFolderViewOptions method, IFolderViewOptions.SetFolderViewOptions, IFolderViewOptions::SetFolderViewOptions, SetFolderViewOptions, SetFolderViewOptions method [Windows Shell], SetFolderViewOptions method [Windows Shell],IFolderViewOptions interface, _shell_IFolderViewOptions_SetFolderViewOptions, shell.IFolderViewOptions_SetFolderViewOptions, shobjidl/IFolderViewOptions::SetFolderViewOptions
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
 - IFolderViewOptions.SetFolderViewOptions
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFolderViewOptions::SetFolderViewOptions


## -description


Sets specified options for the view.


## -parameters




### -param fvoMask [in]

Type: <b><a href="https://msdn.microsoft.com/ab0ebc82-e917-4e3a-864b-fc3bb6280a48">FOLDERVIEWOPTIONS</a></b>

A bitmask made up of one or more of the <a href="https://msdn.microsoft.com/ab0ebc82-e917-4e3a-864b-fc3bb6280a48">FOLDERVIEWOPTIONS</a> flags to indicate which options' are being changed. Values in <i>fvoFlags</i> not included in this mask are ignored.


### -param fvoFlags [in]

Type: <b><a href="https://msdn.microsoft.com/ab0ebc82-e917-4e3a-864b-fc3bb6280a48">FOLDERVIEWOPTIONS</a></b>

A bitmask that contains the new values for the options specified in <i>fvoMask</i>. To enable an option, the bitmask should include the <a href="https://msdn.microsoft.com/ab0ebc82-e917-4e3a-864b-fc3bb6280a48">FOLDERVIEWOPTIONS</a> flag for that option. To disable an option, the bit used for that <b>FOLDERVIEWOPTIONS</b> flag should be 0.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



