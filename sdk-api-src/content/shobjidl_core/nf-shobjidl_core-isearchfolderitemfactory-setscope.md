---
UID: NF:shobjidl_core.ISearchFolderItemFactory.SetScope
title: ISearchFolderItemFactory::SetScope
author: windows-sdk-content
description: Sets search scope, as specified.
old-location: shell\ISearchFolderItemFactory_SetScope.htm
tech.root: shell
ms.assetid: 0dd87a75-f172-4294-81cb-95207b04b3c5
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: ISearchFolderItemFactory interface [Windows Shell],SetScope method, ISearchFolderItemFactory.SetScope, ISearchFolderItemFactory::SetScope, SetScope, SetScope method [Windows Shell], SetScope method [Windows Shell],ISearchFolderItemFactory interface, _shell_ISearchFolderItemFactory_SetScope, shell.ISearchFolderItemFactory_SetScope, shobjidl_core/ISearchFolderItemFactory::SetScope
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
 - ISearchFolderItemFactory.SetScope
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISearchFolderItemFactory::SetScope


## -description


Sets search scope, as specified.


## -parameters




### -param psiaScope [in]

Type: <b><a href="https://msdn.microsoft.com/348213d1-c03f-4c38-9d13-3b1009d94e07">IShellItemArray</a>*</b>

A pointer to the list of locations to search. The search will include this location and all its subcontainers. The default is <b>FOLDERID_Profile</b>


## -returns



Type: <b>HRESULT</b>

Returns a success value if successful, or an error value otherwise.



