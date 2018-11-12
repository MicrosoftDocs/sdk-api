---
UID: NF:shobjidl_core.ITaskbarList3.UnregisterTab
title: ITaskbarList3::UnregisterTab
author: windows-sdk-content
description: Removes a thumbnail from an application's preview group when that tab or document is closed in the application.
old-location: shell\ITaskbarList3_UnregisterTab.htm
tech.root: shell
ms.assetid: 667cafde-f693-46c3-bbec-140fc7cade5d
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: ITaskbarList3 interface [Windows Shell],UnregisterTab method, ITaskbarList3.UnregisterTab, ITaskbarList3::UnregisterTab, UnregisterTab, UnregisterTab method [Windows Shell], UnregisterTab method [Windows Shell],ITaskbarList3 interface, _shell_ITaskbarList3_UnregisterTab, shell.ITaskbarList3_UnregisterTab, shobjidl_core/ITaskbarList3::UnregisterTab
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
req.lib: Explorerframe.lib
req.dll: Explorerframe.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Explorerframe.dll
api_name:
 - ITaskbarList3.UnregisterTab
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITaskbarList3::UnregisterTab


## -description


Removes a thumbnail from an application's preview group when that tab or document is closed in the application.


## -parameters




### -param hwndTab [in]

Type: <b>HWND</b>

The handle of the tab window whose thumbnail is being removed. This is the same value with which the thumbnail was registered as part the group through <a href="https://msdn.microsoft.com/b0cdca51-108a-4507-bd9e-6bcd4386c36a">ITaskbarList3::RegisterTab</a>. This value is required and cannot be <b>NULL</b>.


## -returns



Type: <b>HRESULT</b>

Returns <b>S_OK</b> if successful, or an error value otherwise. If <i>hwndTab</i> is <b>NULL</b>, this method returns an error.




## -remarks



It is the responsibility of the calling application to free <i>hwndTab</i> through <a href="https://msdn.microsoft.com/054fa847-7d6e-4c73-bf8c-b75203713b3e">DestroyWindow</a>. <b>UnregisterTab</b> must be called before the handle is freed.




## -see-also




<a href="https://msdn.microsoft.com/c63f5fe8-4a8f-4ca8-bd6a-7733110bbb38">ITaskbarList</a>



<a href="https://msdn.microsoft.com/8af23586-349f-4d21-98cb-0aaa27a586ff">ITaskbarList2</a>



<a href="https://msdn.microsoft.com/a5eb4e5a-df17-4aca-96fb-d8475e266b92">ITaskbarList3</a>



<a href="https://msdn.microsoft.com/b0cdca51-108a-4507-bd9e-6bcd4386c36a">ITaskbarList3::RegisterTab</a>



<a href="https://msdn.microsoft.com/d82f11eb-bfff-4661-8e2e-520f8226809b">ITaskbarList3::SetTabActive</a>



<a href="https://msdn.microsoft.com/a35342fd-448b-48cf-8400-30f4b7776bbf">ITaskbarList3::SetTabOrder</a>



<a href="https://msdn.microsoft.com/cbf2b07d-d67c-4755-888c-d40692d13cae">Taskbar Extensions</a>
 

 

