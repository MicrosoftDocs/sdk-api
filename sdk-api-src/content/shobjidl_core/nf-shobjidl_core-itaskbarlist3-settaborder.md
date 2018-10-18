---
UID: NF:shobjidl_core.ITaskbarList3.SetTabOrder
title: ITaskbarList3::SetTabOrder
author: windows-sdk-content
description: Inserts a new thumbnail into a tabbed-document interface (TDI) or multiple-document interface (MDI) application's group flyout or moves an existing thumbnail to a new position in the application's group.
old-location: shell\ITaskbarList3_SetTabOrder.htm
tech.root: shell
ms.assetid: a35342fd-448b-48cf-8400-30f4b7776bbf
ms.author: windowssdkdev
ms.date: 10/17/2018
ms.keywords: ITaskbarList3 interface [Windows Shell],SetTabOrder method, ITaskbarList3.SetTabOrder, ITaskbarList3::SetTabOrder, SetTabOrder, SetTabOrder method [Windows Shell], SetTabOrder method [Windows Shell],ITaskbarList3 interface, _shell_ITaskbarList3_SetTabOrder, shell.ITaskbarList3_SetTabOrder, shobjidl_core/ITaskbarList3::SetTabOrder
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
 - ITaskbarList3.SetTabOrder
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITaskbarList3::SetTabOrder


## -description


Inserts a new thumbnail into a tabbed-document interface (TDI) or multiple-document interface (MDI) application's group flyout or moves an existing thumbnail to a new position in the application's group.


## -parameters




### -param hwndTab [in]

Type: <b>HWND</b>

The handle of the tab window whose thumbnail is being placed. This value is required, must already be registered through <a href="https://msdn.microsoft.com/b0cdca51-108a-4507-bd9e-6bcd4386c36a">ITaskbarList3::RegisterTab</a>, and cannot be <b>NULL</b>.


### -param hwndInsertBefore [in, optional]

Type: <b>HWND</b>

The handle of the tab window whose thumbnail that <i>hwndTab</i> is inserted to the left of. This handle must already be registered through <a href="https://msdn.microsoft.com/b0cdca51-108a-4507-bd9e-6bcd4386c36a">ITaskbarList3::RegisterTab</a>. If this value is <b>NULL</b>, the new thumbnail is added to the end of the list.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method must be called for the thumbnail to be shown in the group. Call it after you have called <a href="https://msdn.microsoft.com/b0cdca51-108a-4507-bd9e-6bcd4386c36a">ITaskbarList3::RegisterTab</a>.




## -see-also




<a href="https://msdn.microsoft.com/c63f5fe8-4a8f-4ca8-bd6a-7733110bbb38">ITaskbarList</a>



<a href="https://msdn.microsoft.com/8af23586-349f-4d21-98cb-0aaa27a586ff">ITaskbarList2</a>



<a href="https://msdn.microsoft.com/a5eb4e5a-df17-4aca-96fb-d8475e266b92">ITaskbarList3</a>



<a href="https://msdn.microsoft.com/b0cdca51-108a-4507-bd9e-6bcd4386c36a">ITaskbarList3::RegisterTab</a>



<a href="https://msdn.microsoft.com/d82f11eb-bfff-4661-8e2e-520f8226809b">ITaskbarList3::SetTabActive</a>



<a href="https://msdn.microsoft.com/667cafde-f693-46c3-bbec-140fc7cade5d">ITaskbarList3::UnregisterTab</a>



<a href="https://msdn.microsoft.com/cbf2b07d-d67c-4755-888c-d40692d13cae">Taskbar Extensions</a>
 

 

