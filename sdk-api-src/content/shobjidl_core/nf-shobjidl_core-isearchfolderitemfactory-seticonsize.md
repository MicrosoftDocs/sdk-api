---
UID: NF:shobjidl_core.ISearchFolderItemFactory.SetIconSize
title: ISearchFolderItemFactory::SetIconSize
author: windows-sdk-content
description: Sets the search folder icon size, as specified. The default settings are based on the FolderTypeID which is set by the ISearchFolderItemFactory::SetFolderTypeID method.
old-location: shell\ISearchFolderItemFactory_SetIconSize.htm
tech.root: shell
ms.assetid: a9a6650f-d9fe-43e8-aed5-9a7006883148
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: ISearchFolderItemFactory interface [Windows Shell],SetIconSize method, ISearchFolderItemFactory.SetIconSize, ISearchFolderItemFactory::SetIconSize, SetIconSize, SetIconSize method [Windows Shell], SetIconSize method [Windows Shell],ISearchFolderItemFactory interface, _shell_ISearchFolderItemFactory_SetIconSize, shell.ISearchFolderItemFactory_SetIconSize, shobjidl_core/ISearchFolderItemFactory::SetIconSize
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - ISearchFolderItemFactory.SetIconSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- shobjidl_core.h
: 
- ISearchFolderItemFactory.SetIconSize
: 
---

# ISearchFolderItemFactory::SetIconSize


## -description


Sets the search folder icon size, as specified. The default settings are based on the <code>FolderTypeID</code> which is set by the <a href="https://msdn.microsoft.com/a9b09dc6-751e-4d5f-b016-0b26c15c68f6">ISearchFolderItemFactory::SetFolderTypeID</a> method.


## -parameters




### -param iIconSize [in]

Type: <b>int</b>

The icon size.


## -returns



Type: <b>HRESULT</b>

Returns a success value if successful, or an error value otherwise.



