---
UID: NF:shobjidl_core.IAttachmentExecute.SetClientTitle
title: IAttachmentExecute::SetClientTitle
author: windows-sdk-content
description: Specifies and stores the title of the prompt window.
old-location: shell\IAttachmentExecute_SetClientTitle.htm
tech.root: shell
ms.assetid: 24840acd-c2d1-43d8-99aa-8614e55d6604
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IAttachmentExecute interface [Windows Shell],SetClientTitle method, IAttachmentExecute.SetClientTitle, IAttachmentExecute::SetClientTitle, SetClientTitle, SetClientTitle method [Windows Shell], SetClientTitle method [Windows Shell],IAttachmentExecute interface, _win32_IAttachmentExecute_SetClientTitle, shell.IAttachmentExecute_SetClientTitle, shobjidl_core/IAttachmentExecute::SetClientTitle
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
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
req.dll: Shdocvw.dll (version 6.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shdocvw.dll
api_name:
 - IAttachmentExecute.SetClientTitle
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
- IAttachmentExecute.SetClientTitle
: 
---

# IAttachmentExecute::SetClientTitle


## -description


Specifies and stores the title of the prompt window.


## -parameters




### -param pszTitle [in]

Type: <b>LPCWSTR</b>

A pointer to a string that contains the title text.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If <b>IAttachmentExecute::SetClientTitle</b> is not called, a default title of <b>File Download</b> is used in the prompt's title bar.



