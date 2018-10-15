---
UID: NF:shobjidl_core.ITaskbarList3.RegisterTab
title: ITaskbarList3::RegisterTab
author: windows-sdk-content
description: Informs the taskbar that a new tab or document thumbnail has been provided for display in an application's taskbar group flyout.
old-location: shell\ITaskbarList3_RegisterTab.htm
tech.root: shell
ms.assetid: b0cdca51-108a-4507-bd9e-6bcd4386c36a
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: ITaskbarList3 interface [Windows Shell],RegisterTab method, ITaskbarList3.RegisterTab, ITaskbarList3::RegisterTab, RegisterTab, RegisterTab method [Windows Shell], RegisterTab method [Windows Shell],ITaskbarList3 interface, _shell_ITaskbarList3_RegisterTab, shell.ITaskbarList3_RegisterTab, shobjidl_core/ITaskbarList3::RegisterTab
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
 - ITaskbarList3.RegisterTab
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITaskbarList3::RegisterTab


## -description


Informs the taskbar that a new tab or document thumbnail has been provided for display in an application's taskbar group flyout.


## -parameters




### -param hwndTab [in]

Type: <b>HWND</b>

Handle of the tab or document window. This value is required and cannot be <b>NULL</b>.


### -param hwndMDI [in]

Type: <b>HWND</b>

Handle of the application's main window. This value tells the taskbar which application's preview group to attach the new thumbnail to. This value is required and cannot be <b>NULL</b>.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or an error value otherwise. If either parameter is <b>NULL</b>, this method returns an error.




## -remarks



By itself, registering a tab thumbnail alone will not result in its being displayed. You must also call <a href="https://msdn.microsoft.com/a35342fd-448b-48cf-8400-30f4b7776bbf">ITaskbarList3::SetTabOrder</a> to instruct the group where to display it.




## -see-also




<a href="https://msdn.microsoft.com/c63f5fe8-4a8f-4ca8-bd6a-7733110bbb38">ITaskbarList</a>



<a href="https://msdn.microsoft.com/8af23586-349f-4d21-98cb-0aaa27a586ff">ITaskbarList2</a>



<a href="https://msdn.microsoft.com/a5eb4e5a-df17-4aca-96fb-d8475e266b92">ITaskbarList3</a>



<a href="https://msdn.microsoft.com/d82f11eb-bfff-4661-8e2e-520f8226809b">ITaskbarList3::SetTabActive</a>



<a href="https://msdn.microsoft.com/a35342fd-448b-48cf-8400-30f4b7776bbf">ITaskbarList3::SetTabOrder</a>



<a href="https://msdn.microsoft.com/667cafde-f693-46c3-bbec-140fc7cade5d">ITaskbarList3::UnregisterTab</a>



<a href="https://msdn.microsoft.com/cbf2b07d-d67c-4755-888c-d40692d13cae">Taskbar Extensions</a>
 

 

