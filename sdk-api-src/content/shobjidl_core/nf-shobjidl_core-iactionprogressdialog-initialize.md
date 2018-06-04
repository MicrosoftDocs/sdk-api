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

# IActionProgressDialog::Initialize


## -description


Provides details about the action progress dialog.


## -parameters




### -param flags [in]

Type: <b>SPINITF</b>

One of the following values.



#### SPINITF_NORMAL (0x01)

Use the default progress dialog behavior.



#### SPINITF_MODAL (0x01)

Use a modal window for the dialog.



#### SPINITF_NOMINIMIZE (0x08)

Do not display a minimize button.


### -param pszTitle [in]

Type: <b>LPCWSTR</b>

The title of the progress dialog.


### -param pszCancel [in]

Type: <b>LPCWSTR</b>

The string displayed when a user closes the dialog before completion.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



