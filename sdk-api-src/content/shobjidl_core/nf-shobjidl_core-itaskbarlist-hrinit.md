---
UID: NF:shobjidl_core.ITaskbarList.HrInit
title: ITaskbarList::HrInit (shobjidl_core.h)
description: Initializes the taskbar list object. This method must be called before any other ITaskbarList methods can be called.
helpviewer_keywords: ["HrInit","HrInit method [Windows Shell]","HrInit method [Windows Shell]","ITaskbarList interface","ITaskbarList interface [Windows Shell]","HrInit method","ITaskbarList.HrInit","ITaskbarList::HrInit","_win32_ITaskbarList_HrInit","shell.ITaskbarList_HrInit","shobjidl_core/ITaskbarList::HrInit"]
old-location: shell\ITaskbarList_HrInit.htm
tech.root: shell
ms.assetid: 0344bf0b-b460-4516-88eb-09131cc9a4f8
ms.date: 12/05/2018
ms.keywords: HrInit, HrInit method [Windows Shell], HrInit method [Windows Shell],ITaskbarList interface, ITaskbarList interface [Windows Shell],HrInit method, ITaskbarList.HrInit, ITaskbarList::HrInit, _win32_ITaskbarList_HrInit, shell.ITaskbarList_HrInit, shobjidl_core/ITaskbarList::HrInit
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
req.lib: 
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITaskbarList::HrInit
 - shobjidl_core/ITaskbarList::HrInit
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - ITaskbarList.HrInit
---

# ITaskbarList::HrInit


## -description

Initializes the taskbar list object. This method must be called before any other <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist">ITaskbarList</a> methods can be called.



## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or an error value otherwise. If the method fails, no other methods can be called. The calling application should release the interface pointer.
