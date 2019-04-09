---
UID: NF:shobjidl_core.IKnownFolder.GetIDList
title: IKnownFolder::GetIDList (shobjidl_core.h)
author: windows-sdk-content
description: Gets the location of the Shell namespace folder in the IDList (ITEMIDLIST) form.
old-location: shell\IKnownFolder_GetIDList.htm
tech.root: shell
ms.assetid: b1c77198-da52-4f74-9e20-56b6d1d450f5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetIDList, GetIDList method [Windows Shell], GetIDList method [Windows Shell],IKnownFolder interface, IKnownFolder interface [Windows Shell],GetIDList method, IKnownFolder.GetIDList, IKnownFolder::GetIDList, _shell_IKnownFolder_GetIDList, shell.IKnownFolder_GetIDList, shobjidl_core/IKnownFolder::GetIDList
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
req.dll: Shell32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IKnownFolder.GetIDList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IKnownFolder::GetIDList


## -description


Gets the location of the Shell namespace folder in the IDList (<a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a>) form.


## -parameters




### -param dwFlags [in]

Type: <b>DWORD</b>

Flags that specify special retrieval options. This value can be 0; otherwise, one or more of the <a href="https://msdn.microsoft.com/7f99fb6c-32f2-4fd8-ad11-3ad84d17c5c1">KNOWN_FOLDER_FLAG</a> values.


### -param ppidl [out]

Type: <b>PIDLIST_ABSOLUTE*</b>

When this method returns, contains the address of an absolute PIDL. This parameter is passed uninitialized. The calling application is responsible for freeing this resource when it is no longer needed.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Equivalent to <a href="https://msdn.microsoft.com/fed9cfb8-4c38-4947-99aa-278245148136">SHGetKnownFolderIDList</a>.




## -see-also




<a href="https://msdn.microsoft.com/dbade93d-73f6-401b-9986-4e6fd439c874">IKnownFolder</a>



<a href="https://msdn.microsoft.com/49799A9E-BA86-4977-B5F3-590BE1E5FBF6">Known Folders Sample</a>



<a href="https://msdn.microsoft.com/fed9cfb8-4c38-4947-99aa-278245148136">SHGetKnownFolderIDList</a>
 

 

