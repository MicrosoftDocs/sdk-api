---
UID: NF:shobjidl_core.IInputObjectSite.OnFocusChangeIS
title: IInputObjectSite::OnFocusChangeIS
author: windows-driver-content
description: Informs the browser that the focus has changed.
old-location: shell\IInputObjectSite_OnFocusChangeIS.htm
old-project: shell
ms.assetid: b779beea-534b-4cf0-9426-db2bbcb52277
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: IInputObjectSite interface [Windows Shell],OnFocusChangeIS method, IInputObjectSite.OnFocusChangeIS, IInputObjectSite::OnFocusChangeIS, OnFocusChangeIS, OnFocusChangeIS method [Windows Shell], OnFocusChangeIS method [Windows Shell],IInputObjectSite interface, _win32_IInputObjectSite_OnFocusChangeIS, shell.IInputObjectSite_OnFocusChangeIS, shobjidl_core/IInputObjectSite::OnFocusChangeIS
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shlobj.h
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Shell32.dll
api_name:
-	IInputObjectSite.OnFocusChangeIS
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
req.product: Outlook Express 6.0
---

# IInputObjectSite::OnFocusChangeIS


## -description


Informs the browser that the focus has changed.


## -parameters




### -param punkObj

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>*</b>

The address of the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface of the object gaining or losing the focus.


### -param fSetFocus

Type: <b>BOOL</b>

Indicates if the object has gained or lost the focus. If this value is nonzero, the object has gained the focus. If this value is zero, the object has lost the focus.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if the method was successful, or a COM-defined error code otherwise.




## -remarks



The calling object should call this method whenever one of its windows gains or loses the input focus.



