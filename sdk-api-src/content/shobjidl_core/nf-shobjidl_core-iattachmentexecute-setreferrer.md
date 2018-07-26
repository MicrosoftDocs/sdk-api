---
UID: NF:shobjidl_core.IAttachmentExecute.SetReferrer
title: IAttachmentExecute::SetReferrer
author: windows-sdk-content
description: Sets the security zone associated with the attachment file based on the referring file.
old-location: shell\IAttachmentExecute_SetReferrer.htm
old-project: shell
ms.assetid: d7ee869a-2afe-4d98-a0bb-d80e57425079
ms.author: windowssdkdev
ms.date: 07/20/2018
ms.keywords: IAttachmentExecute interface [Windows Shell],SetReferrer method, IAttachmentExecute.SetReferrer, IAttachmentExecute::SetReferrer, SetReferrer, SetReferrer method [Windows Shell], SetReferrer method [Windows Shell],IAttachmentExecute interface, _win32_IAttachmentExecute_SetReferrer, shell.IAttachmentExecute_SetReferrer, shobjidl_core/IAttachmentExecute::SetReferrer
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
 - IAttachmentExecute.SetReferrer
product: Windows
targetos: Windows
req.lib: 
req.dll: Shdocvw.dll (version 6.0 or later)
req.irql: 
req.product: Outlook Express 6.0
---

# IAttachmentExecute::SetReferrer


## -description


Sets the security zone associated with the attachment file based on the referring file.


## -parameters




### -param pszReferrer [in]

Type: <b>LPCWSTR</b>

A pointer to a string containing the path of the referring file.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<b>IAttachmentExecute::SetReferrer</b> and <a href="https://msdn.microsoft.com/6545252b-1c43-4d62-9784-b63688ef9fdc">IAttachmentExecute::SetSource</a> have similar functionality. If both are set, the least-trusted zone of the two is used.

<b>IAttachmentExecute::SetReferrer</b> is used by container files to indicate indirect inheritance and avoid zone elevation. It can also be used with shortcut files to limit elevation based on parameters.

Calling <b>IAttachmentExecute::SetReferrer</b> is optional.

<b>IAttachmentExecute::SetReferrer</b> is only used to determine the security zone and its associated policies.



