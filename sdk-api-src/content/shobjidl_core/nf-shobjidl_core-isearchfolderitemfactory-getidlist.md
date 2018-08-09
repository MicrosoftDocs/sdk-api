---
UID: NF:shobjidl_core.ISearchFolderItemFactory.GetIDList
title: ISearchFolderItemFactory::GetIDList
author: windows-sdk-content
description: Gets the search folder as an ITEMIDLIST.
old-location: shell\ISearchFolderItemFactory_GetIDList.htm
old-project: shell
ms.assetid: 9547c429-9396-474e-b772-6e3aa28d1937
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetIDList, GetIDList method [Windows Shell], GetIDList method [Windows Shell],ISearchFolderItemFactory interface, ISearchFolderItemFactory interface [Windows Shell],GetIDList method, ISearchFolderItemFactory.GetIDList, ISearchFolderItemFactory::GetIDList, _shell_ISearchFolderItemFactory_GetIDList, shell.ISearchFolderItemFactory_GetIDList, shobjidl_core/ISearchFolderItemFactory::GetIDList
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - ISearchFolderItemFactory.GetIDList
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# ISearchFolderItemFactory::GetIDList


## -description


Gets the search folder as an <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a>.


## -parameters




### -param ppidl [out]

Type: <b>PIDLIST_ABSOLUTE*</b>

When this method returns successfully, contains a PIDL.


## -returns



Type: <b>HRESULT</b>

Returns a success value if successful, or an error value otherwise.




## -see-also




<a href="https://msdn.microsoft.com/a684b373-6de4-4b4a-bbae-85e1c5a7e04a">ISearchFolderItemFactory</a>



<a href="https://msdn.microsoft.com/42821075-8123-4bfa-a6ba-8d3a77a9f50b">SHGetIDListFromObject</a>
 

 

