---
UID: NF:shobjidl_core.ISearchFolderItemFactory.SetStacks
title: ISearchFolderItemFactory::SetStacks
author: windows-sdk-content
description: Creates a list of stack keys, as specified. If this method is not called, by default the folder will not be stacked.
old-location: shell\ISearchFolderItemFactory_SetStacks.htm
tech.root: shell
ms.assetid: d2f3d975-b968-4491-868f-90eccb40e8e4
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: ISearchFolderItemFactory interface [Windows Shell],SetStacks method, ISearchFolderItemFactory.SetStacks, ISearchFolderItemFactory::SetStacks, SetStacks, SetStacks method [Windows Shell], SetStacks method [Windows Shell],ISearchFolderItemFactory interface, _shell_ISearchFolderItemFactory_SetStacks, shell.ISearchFolderItemFactory_SetStacks, shobjidl_core/ISearchFolderItemFactory::SetStacks
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
 - ISearchFolderItemFactory.SetStacks
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISearchFolderItemFactory::SetStacks


## -description


Creates a list of stack keys, as specified. If this method is not called, by default the folder will not be stacked.


## -parameters




### -param cStackKeys [in]

Type: <b>UINT</b>

The number of stacks keys.


### -param rgStackKeys [in]

Type: <b><a href="https://msdn.microsoft.com/3f5f31af-f040-443b-9045-9761055381ea">PROPERTYKEY</a>*</b>

A pointer to an array of <a href="https://msdn.microsoft.com/3f5f31af-f040-443b-9045-9761055381ea">PROPERTYKEY</a> structures containing stack key information.


## -returns



Type: <b>HRESULT</b>

Returns a success value if successful, or an error value otherwise.



