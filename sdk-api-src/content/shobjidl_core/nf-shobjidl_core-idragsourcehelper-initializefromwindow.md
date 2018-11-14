---
UID: NF:shobjidl_core.IDragSourceHelper.InitializeFromWindow
title: IDragSourceHelper::InitializeFromWindow
author: windows-sdk-content
description: Initializes the drag-image manager for a control with a window.
old-location: shell\IDragSourceHelper_InitializeFromWindow.htm
tech.root: shell
ms.assetid: 0bcdfe92-cec0-44f3-a345-5b560d52fae9
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IDragSourceHelper interface [Windows Shell],InitializeFromWindow method, IDragSourceHelper.InitializeFromWindow, IDragSourceHelper::InitializeFromWindow, InitializeFromWindow, InitializeFromWindow method [Windows Shell], InitializeFromWindow method [Windows Shell],IDragSourceHelper interface, _win32_IDragSourceHelper_InitializeFromWindow, shell.IDragSourceHelper_InitializeFromWindow, shobjidl_core/IDragSourceHelper::InitializeFromWindow
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IDragSourceHelper.InitializeFromWindow
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- shobjidl_core.h
: 
- IDragSourceHelper.InitializeFromWindow
: 
---

# IDragSourceHelper::InitializeFromWindow


## -description


Initializes the drag-image manager for a control with a window.


## -parameters




### -param hwnd [in]

Type: <b>HWND</b>

A handle to the window that receives the <b>DI_GETDRAGIMAGE</b> message. This value can be <b>NULL</b>.


### -param ppt [in]

Type: <b><a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a> structure that specifies the location of the cursor within the drag image. The structure should contain the offset from the upper-left corner of the drag image to the location of the cursor. This value can be <b>NULL</b>.


### -param pDataObject [in]

Type: <b><a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a>*</b>

A pointer to the data object's <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a> interface.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The <b>DI_GETDRAGIMAGE</b> message allows you to source a drag image from a custom control. It is defined in Shlobj.h and must be registered with <a href="https://msdn.microsoft.com/51ddc767-ffce-42bf-885a-24b9ee1b25f0">RegisterWindowMessage</a>. When the window specified by <i>hwnd</i> receives the <b>DI_GETDRAGIMAGE</b> message, the <i>lParam</i> value holds a pointer to an <a href="https://msdn.microsoft.com/e0dd76b2-fd5c-41e8-b540-db90a2f0dcec">SHDRAGIMAGE</a> structure. The handler should fill the structure with the drag image bitmap information.




## -see-also




<a href="https://msdn.microsoft.com/d68ac8fd-4d9c-47ee-bdff-0c5bae6b5e28">IDragSourceHelper</a>
 

 

