---
UID: NF:shobjidl_core.IAttachmentExecute.SetSource
title: IAttachmentExecute::SetSource (shobjidl_core.h)
author: windows-sdk-content
description: Sets an alternate path or URL for the source of a file transfer.
old-location: shell\IAttachmentExecute_SetSource.htm
tech.root: shell
ms.assetid: 6545252b-1c43-4d62-9784-b63688ef9fdc
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAttachmentExecute interface [Windows Shell],SetSource method, IAttachmentExecute.SetSource, IAttachmentExecute::SetSource, SetSource, SetSource method [Windows Shell], SetSource method [Windows Shell],IAttachmentExecute interface, _win32_IAttachmentExecute_SetSource, shell.IAttachmentExecute_SetSource, shobjidl_core/IAttachmentExecute::SetSource
ms.topic: method
f1_keywords: ["shobjidl_core/IAttachmentExecute.SetSource"]
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
 - IAttachmentExecute.SetSource
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAttachmentExecute::SetSource


## -description


Sets an alternate path or URL for the source of a file transfer.


## -parameters




### -param pszSource [in]

Type: <b>LPCWSTR</b>

A pointer to a string containing the path or URL to use as the source.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The path or URL declared here is used as the primary zone determinant. The policy under which the attachment is handled is based partially on the perceived zone. If <i>pszSource</i> is <b>NULL</b>, the default is Restricted Zone.

Calling <b>IAttachmentExecute::SetSource</b> is optional.

The path or URL declared here can also be used in the prompt UI as the <b>From</b> field.

The path or URL declared here can also be sent to handlers that can process URLs.



