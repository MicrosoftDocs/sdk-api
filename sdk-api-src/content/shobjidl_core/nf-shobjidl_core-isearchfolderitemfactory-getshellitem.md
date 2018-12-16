---
UID: NF:shobjidl_core.ISearchFolderItemFactory.GetShellItem
title: ISearchFolderItemFactory::GetShellItem
author: windows-sdk-content
description: Gets the search folder as a IShellItem.
old-location: shell\ISearchFolderItemFactory_GetShellItem.htm
tech.root: shell
ms.assetid: fc5dd159-8a47-479f-b087-bd161093d0a0
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetShellItem, GetShellItem method [Windows Shell], GetShellItem method [Windows Shell],ISearchFolderItemFactory interface, ISearchFolderItemFactory interface [Windows Shell],GetShellItem method, ISearchFolderItemFactory.GetShellItem, ISearchFolderItemFactory::GetShellItem, _shell_ISearchFolderItemFactory_GetShellItem, shell.ISearchFolderItemFactory_GetShellItem, shobjidl_core/ISearchFolderItemFactory::GetShellItem
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
 - ISearchFolderItemFactory.GetShellItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISearchFolderItemFactory::GetShellItem


## -description


Gets the search folder as a <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>.


## -parameters




### -param riid [in]

Type: <b>REFIID</b>

A reference to the desired IID.


### -param ppv [out]

Type: <b>void**</b>

The <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> interface pointer specified in <i>riid</i>.


## -returns



Type: <b>HRESULT</b>

Returns a success value if successful, or an error value otherwise.




## -remarks



When the retrieved <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> is enumerated, it returns the search results.




## -see-also




<a href="https://msdn.microsoft.com/a684b373-6de4-4b4a-bbae-85e1c5a7e04a">ISearchFolderItemFactory</a>



<a href="https://msdn.microsoft.com/a6dcddd9-cdbc-4cf9-97e3-d1b562283344">SHCreateItemFromIDList</a>
 

 

