---
UID: NF:shobjidl_core.ISearchFolderItemFactory.SetDisplayName
title: ISearchFolderItemFactory::SetDisplayName
author: windows-sdk-content
description: Sets the search folder display name, as specified.
old-location: shell\ISearchFolderItemFactory_SetDisplayName.htm
tech.root: shell
ms.assetid: 2552677b-7907-4a2b-8a2f-6769bca64029
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: ISearchFolderItemFactory interface [Windows Shell],SetDisplayName method, ISearchFolderItemFactory.SetDisplayName, ISearchFolderItemFactory::SetDisplayName, SetDisplayName, SetDisplayName method [Windows Shell], SetDisplayName method [Windows Shell],ISearchFolderItemFactory interface, _shell_ISearchFolderItemFactory_SetDisplayName, shell.ISearchFolderItemFactory_SetDisplayName, shobjidl_core/ISearchFolderItemFactory::SetDisplayName
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
 - ISearchFolderItemFactory.SetDisplayName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISearchFolderItemFactory::SetDisplayName


## -description


Sets the search folder display name, as specified.


## -parameters




### -param pszDisplayName [in]

Type: <b>LPCWSTR</b>

A pointer to a folder display name as a Unicode string.


## -returns



Type: <b>HRESULT</b>

Returns a success value if successful, or an error value otherwise.




## -remarks



Calling this method is required. A display name must be set.



