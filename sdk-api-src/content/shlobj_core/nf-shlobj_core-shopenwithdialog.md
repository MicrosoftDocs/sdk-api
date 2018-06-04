---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# SHOpenWithDialog function


## -description


Displays the <b>Open With</b> dialog box.


## -parameters




### -param hwndParent [in, optional]

Type: <b>HWND</b>

The handle of the parent window. This value can be <b>NULL</b>.


### -param poainfo [in]

Type: <b>const <a href="https://msdn.microsoft.com/5486c4d3-c6c5-459d-aa7f-426971184876">OPENASINFO</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/5486c4d3-c6c5-459d-aa7f-426971184876">OPENASINFO</a> structure, which specifies the contents of the resulting dialog.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Starting in Windows 10, the <b>OAIF_ALLOW_REGISTRATION</b>, <b>OAIF_FORCE_REGISTRATION</b>, and <b>OAIF_HIDE_REGISTRATION</b> flags will be ignored by <b>SHOpenWithDialog</b>. The <b>Open With</b> dialog box can no longer be used to change the default program used to open a file extension. You can only use <b>SHOpenWithDialog</b> to open a single file.

If <b>SHOpenWithDialog</b> is called without passing <b>OAIF_EXEC</b>, the user will receive a dialog that informs them that they can change the default programs used to open file extensions in their <b>Settings</b>.



