---
UID: NF:shobjidl_core.IApplicationDocumentLists.SetAppID
title: IApplicationDocumentLists::SetAppID
author: windows-sdk-content
description: Specifies a unique Application User Model ID (AppUserModelID) for the application whose destination lists are being retrieved. This method is optional.
old-location: shell\IApplicationDocumentLists_SetAppID.htm
tech.root: shell
ms.assetid: 1c5135c1-b98d-4d27-8437-5ca57af9a525
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: IApplicationDocumentLists interface [Windows Shell],SetAppID method, IApplicationDocumentLists.SetAppID, IApplicationDocumentLists::SetAppID, SetAppID, SetAppID method [Windows Shell], SetAppID method [Windows Shell],IApplicationDocumentLists interface, _shell_IApplicationDocumentLists_SetAppID, shell.IApplicationDocumentLists_SetAppID, shobjidl_core/IApplicationDocumentLists::SetAppID
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
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
req.lib: Shell32.lib
req.dll: Shell32.dll (version 6.1 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IApplicationDocumentLists.SetAppID
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IApplicationDocumentLists::SetAppID


## -description


Specifies a unique Application User Model ID (AppUserModelID) for the application whose destination lists are being retrieved. This method is optional.


## -parameters




### -param pszAppID [in]

Type: <b>LPCWSTR</b>

A pointer to the AppUserModelID of the process whose taskbar button representation receives the Jump List.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If the application has an explicit AppUserModelID, this method must be called before you call <a href="https://msdn.microsoft.com/d86bf039-81d9-4d43-9671-b107d7e925ab">GetList</a>.

After an AppUserModelID is specified through an object's <b>SetAppID</b> method, the AppUserModelID is saved in the object for that object's lifetime, providing that it is not overwritten by another call to <b>SetAppID</b>.

Some applications will not declare an explicit AppUserModelID and should not call this method. In that case, the application's identity is deduced when <a href="https://msdn.microsoft.com/d86bf039-81d9-4d43-9671-b107d7e925ab">IApplicationDocumentLists::GetList</a> is called. However, there is a performance benefit in avoiding those calculations, so applications that provide custom Jump Lists are encouraged to use <a href="https://msdn.microsoft.com/2b8baf6d-9c9a-4727-9deb-3d335bd0dc7c">explicit AppUserModelIDs</a>.




## -see-also




<a href="https://msdn.microsoft.com/ebce2d99-6f20-4545-9f12-d79cd8d0828f">Application User Model IDs (AppUserModelIDs)</a>



<a href="https://msdn.microsoft.com/1912d8fd-1724-4a4b-b74a-e05db12ffead">IApplicationDocumentLists</a>



<a href="https://msdn.microsoft.com/cbf2b07d-d67c-4755-888c-d40692d13cae">Taskbar Extensions</a>
 

 

