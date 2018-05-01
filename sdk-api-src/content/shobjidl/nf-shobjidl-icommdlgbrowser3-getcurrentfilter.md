---
UID: NF:shobjidl.ICommDlgBrowser3.GetCurrentFilter
title: ICommDlgBrowser3::GetCurrentFilter method
author: windows-driver-content
description: Gets the current filter as a Unicode string.
old-location: shell\ICommDlgBrowser3_GetCurrentFilter.htm
old-project: shell
ms.assetid: 038f3478-82d0-4023-a787-b7a2c66ceb27
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetCurrentFilter method [Windows Shell], GetCurrentFilter method [Windows Shell], ICommDlgBrowser3 interface, GetCurrentFilter,ICommDlgBrowser3.GetCurrentFilter, ICommDlgBrowser3, ICommDlgBrowser3 interface [Windows Shell], GetCurrentFilter method, ICommDlgBrowser3::GetCurrentFilter, _shell_ICommDlgBrowser3_GetCurrentFilter, shell.ICommDlgBrowser3_GetCurrentFilter, shobjidl/ICommDlgBrowser3::GetCurrentFilter
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: VPWATERMARKFLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Shobjidl.h
api_name:
-	ICommDlgBrowser3.GetCurrentFilter
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# ICommDlgBrowser3::GetCurrentFilter method


## -description


Gets the current filter as a Unicode string.


## -parameters




### -param pszFileSpec [out]

Type: <b>LPWSTR</b>

Contains a pointer to the current filter path/file as a Unicode string.


### -param cchFileSpec [in]

Type: <b>int</b>

Specifies the path/file length, in characters.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



