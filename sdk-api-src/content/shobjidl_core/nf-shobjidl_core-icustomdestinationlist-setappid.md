---
UID: NF:shobjidl_core.ICustomDestinationList.SetAppID
title: ICustomDestinationList::SetAppID
author: windows-sdk-content
description: Specifies a unique Application User Model ID (AppUserModelID) for the application whose taskbar button will hold the custom Jump List built through the methods of this interface. This method is optional.
old-location: shell\ICustomDestinationList_SetAppID.htm
tech.root: shell
ms.assetid: 7b3a5d32-bf44-4c4f-9b31-6c0a82aac6fd
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: ICustomDestinationList interface [Windows Shell],SetAppID method, ICustomDestinationList.SetAppID, ICustomDestinationList::SetAppID, SetAppID, SetAppID method [Windows Shell], SetAppID method [Windows Shell],ICustomDestinationList interface, _shell_ICustomDestinationList_SetAppID, shell.ICustomDestinationList_SetAppID, shobjidl_core/ICustomDestinationList::SetAppID
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
 - ICustomDestinationList.SetAppID
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICustomDestinationList::SetAppID


## -description


Specifies a unique Application User Model ID (AppUserModelID) for the application whose taskbar button will hold the custom Jump List built through the methods of this interface. This method is optional.


## -parameters




### -param pszAppID [in]

Type: <b>LPCWSTR</b>

A pointer to the AppUserModelID of the process or application whose taskbar representation receives the Jump List.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or an error value otherwise, including the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
This method was called after <a href="https://msdn.microsoft.com/431ae6b0-1421-46ec-a06a-38158acb0275">ICustomDestinationList::BeginList</a>. The list-building process is already running with a particular AppUserModelID, either inferred by the system or set through a call to <a href="https://msdn.microsoft.com/7b3a5d32-bf44-4c4f-9b31-6c0a82aac6fd">SetAppID</a> before the call to <b>BeginList</b>. After a list-building operation is in progress, the AppUserModelID cannot be changed until after <a href="https://msdn.microsoft.com/5f9aa598-9a94-4210-84cd-f4b39e47b260">CommitList</a> or <a href="https://msdn.microsoft.com/922eb957-8031-4b4c-9b13-78a86f199bfa">AbortList</a> has been called.

</td>
</tr>
</table>
 




## -remarks



If an application has an explicit AppUserModelID, you must call <b>SetAppID</b> before you call <a href="https://msdn.microsoft.com/431ae6b0-1421-46ec-a06a-38158acb0275">ICustomDestinationList::BeginList</a> or <a href="https://msdn.microsoft.com/705763cf-a97f-430f-bfc3-916e943668ef">ICustomDestinationList::GetRemovedDestinations</a>.

After an AppUserModelID is specified through an object's <b>SetAppID</b> method, the AppUserModelID is saved in the object for that object's lifetime, providing that it is not overwritten by another call to <b>SetAppID</b>.

Some applications will not declare an explicit AppUserModelID and should not call this method. In that case, the application's identity is deduced when <a href="https://msdn.microsoft.com/431ae6b0-1421-46ec-a06a-38158acb0275">ICustomDestinationList::BeginList</a> or <a href="https://msdn.microsoft.com/705763cf-a97f-430f-bfc3-916e943668ef">ICustomDestinationList::GetRemovedDestinations</a> are called. However, there is a performance benefit in avoiding those calculations, so applications that provide custom Jump Lists are encouraged to use <a href="https://msdn.microsoft.com/2b8baf6d-9c9a-4727-9deb-3d335bd0dc7c">explicit AppUserModelIDs</a>.




## -see-also




<a href="https://msdn.microsoft.com/ebce2d99-6f20-4545-9f12-d79cd8d0828f">Application User Model IDs (AppUserModelIDs)</a>



<a href="https://msdn.microsoft.com/65a3dab8-3136-416d-bd8a-ca813bfe0533">ICustomDestinationList</a>



<a href="https://msdn.microsoft.com/2b8baf6d-9c9a-4727-9deb-3d335bd0dc7c">SetCurrentProcessExplicitAppUserModelID</a>



<a href="https://msdn.microsoft.com/cbf2b07d-d67c-4755-888c-d40692d13cae">Taskbar Extensions</a>
 

 

