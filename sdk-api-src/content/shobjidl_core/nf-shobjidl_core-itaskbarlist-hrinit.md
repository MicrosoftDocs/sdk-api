---
UID: NF:shobjidl_core.ITaskbarList.HrInit
title: ITaskbarList::HrInit
author: windows-sdk-content
description: Initializes the taskbar list object. This method must be called before any other ITaskbarList methods can be called.
old-location: shell\ITaskbarList_HrInit.htm
old-project: shell
ms.assetid: 0344bf0b-b460-4516-88eb-09131cc9a4f8
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: HrInit, HrInit method [Windows Shell], HrInit method [Windows Shell],ITaskbarList interface, ITaskbarList interface [Windows Shell],HrInit method, ITaskbarList.HrInit, ITaskbarList::HrInit, _win32_ITaskbarList_HrInit, shell.ITaskbarList_HrInit, shobjidl_core/ITaskbarList::HrInit
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Shell32.dll
api_name:
-	ITaskbarList.HrInit
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
req.product: Outlook Express 6.0
---

# ITaskbarList::HrInit


## -description


Initializes the taskbar list object. This method must be called before any other <a href="https://msdn.microsoft.com/c63f5fe8-4a8f-4ca8-bd6a-7733110bbb38">ITaskbarList</a> methods can be called.


## -parameters






## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or an error value otherwise. If the method fails, no other methods can be called. The calling application should release the interface pointer.



