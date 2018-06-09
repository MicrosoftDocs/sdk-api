---
UID: NF:shobjidl_core.IShellView.GetItemObject
title: IShellView::GetItemObject
author: windows-sdk-content
description: Gets an interface that refers to data presented in the view.
old-location: shell\IShellView_GetItemObject.htm
old-project: shell
ms.assetid: 249ce8cc-6820-4f0a-a83a-2035e88d0d9c
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: GetItemObject, GetItemObject method [Windows Shell], GetItemObject method [Windows Shell],IShellView interface, IShellView interface [Windows Shell],GetItemObject method, IShellView.GetItemObject, IShellView::GetItemObject, _win32_IShellView_GetItemObject, shell.IShellView_GetItemObject, shobjidl_core/IShellView::GetItemObject
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - Shell32.dll
api_name:
 - IShellView.GetItemObject
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
req.product: Outlook Express 6.0
---

# IShellView::GetItemObject


## -description


Gets an interface that refers to data presented in the view.


## -parameters




### -param uItem

Type: <b>UINT</b>

The constants that refer to an aspect of the view. This parameter can be any one of the <a href="https://msdn.microsoft.com/06ed616b-8121-4ea0-bd05-632888d0f376">_SVGIO</a> constants.


### -param riid

Type: <b>REFIID</b>

The identifier of the COM interface being requested.


### -param ppv

Type: <b>LPVOID*</b>

The address that receives the interface pointer. If an error occurs, the pointer returned must be <b>NULL</b>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Used by the common dialog boxes to retrieve the selected items from the view.




## -see-also




<a href="https://msdn.microsoft.com/91438583-e4f1-456f-a130-2a45846fd725">IShellView</a>
 

 

