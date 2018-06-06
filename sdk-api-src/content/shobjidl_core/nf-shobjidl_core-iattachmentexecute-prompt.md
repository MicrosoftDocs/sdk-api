---
UID: NF:shobjidl_core.IAttachmentExecute.Prompt
title: IAttachmentExecute::Prompt
author: windows-sdk-content
description: Presents a prompt UI to the user.
old-location: shell\IAttachmentExecute_Prompt.htm
old-project: shell
ms.assetid: 01c01abf-df7a-411b-979b-ddd8da569f91
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IAttachmentExecute interface [Windows Shell],Prompt method, IAttachmentExecute.Prompt, IAttachmentExecute::Prompt, Prompt, Prompt method [Windows Shell], Prompt method [Windows Shell],IAttachmentExecute interface, _win32_IAttachmentExecute_Prompt, shell.IAttachmentExecute_Prompt, shobjidl_core/IAttachmentExecute::Prompt
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shdocvw.dll
api_name:
 - IAttachmentExecute.Prompt
product: Windows
targetos: Windows
req.lib: 
req.dll: Shdocvw.dll (version 6.0 or later)
req.irql: 
req.product: Outlook Express 6.0
---

# IAttachmentExecute::Prompt


## -description


Presents a prompt UI to the user.


## -parameters




### -param hwnd [in]

Type: <b>HWND</b>

A handle to the parent window.


### -param prompt [in]

Type: <b><a href="https://msdn.microsoft.com/a19bdff0-3b02-44f4-906a-2e1b85685c52">ATTACHMENT_PROMPT</a></b>

A member of the <a href="https://msdn.microsoft.com/a19bdff0-3b02-44f4-906a-2e1b85685c52">ATTACHMENT_PROMPT</a> enumeration that indicates what type of prompt UI to display to the user.


### -param paction [out]

Type: <b><a href="https://msdn.microsoft.com/2deeb14b-2665-4970-923c-9da1f561979f">ATTACHMENT_ACTION</a>*</b>

A member of the <a href="https://msdn.microsoft.com/2deeb14b-2665-4970-923c-9da1f561979f">ATTACHMENT_ACTION</a> enumeration that indicates the action to be performed upon user confirmation.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



You must call <a href="https://msdn.microsoft.com/52dc823f-4429-4c1f-8906-9e4ee3f8158e">IAttachmentExecute::SetFileName</a> or <a href="https://msdn.microsoft.com/763ce5a7-bbad-4dd8-a416-86a96f466510">IAttachmentExecute::SetLocalPath</a> before calling <b>IAttachmentExecute::Prompt</b>.

<b>IAttachmentExecute::Prompt</b> can be called by the application to force UI presentation before the file has been copied to disk.



