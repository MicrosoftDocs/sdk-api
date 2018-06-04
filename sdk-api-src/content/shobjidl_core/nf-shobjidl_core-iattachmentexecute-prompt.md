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



