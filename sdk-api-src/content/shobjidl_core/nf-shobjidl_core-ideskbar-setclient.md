---
UID: NF:shobjidl_core.IDeskBar.SetClient
title: IDeskBar::SetClient
author: windows-sdk-content
description: Sets the client specified by punkClient.
old-location: shell\IDeskBar_SetClient.htm
old-project: shell
ms.assetid: 26655738-a2d5-446c-af7f-866b34beb3ab
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IDeskBar interface [Windows Shell],SetClient method, IDeskBar.SetClient, IDeskBar::SetClient, SetClient, SetClient method [Windows Shell], SetClient method [Windows Shell],IDeskBar interface, _win32_IDeskBar_SetClient, shell.IDeskBar_SetClient, shobjidl_core/IDeskBar::SetClient
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Shell32.dll
api_name:
-	IDeskBar.SetClient
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Outlook Express 6.0
---

# IDeskBar::SetClient


## -description


Sets the client specified by <i>punkClient</i>.


## -parameters




### -param punkClient [in, optional]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>*</b>

A pointer to a variable of type <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> that specifies the client used by the desk bar.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



