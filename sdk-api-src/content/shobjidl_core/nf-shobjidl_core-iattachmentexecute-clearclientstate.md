---
UID: NF:shobjidl_core.IAttachmentExecute.ClearClientState
title: IAttachmentExecute::ClearClientState
author: windows-sdk-content
description: Removes any stored state that is based on the client's GUID. An example might be a setting based on a checked box that indicates a prompt should not be displayed again for a particular file type.
old-location: shell\IAttachmentExecute_ClearClientState.htm
old-project: shell
ms.assetid: 238e78be-3306-4ac5-95a9-c7fa48c1c4fe
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: ClearClientState, ClearClientState method [Windows Shell], ClearClientState method [Windows Shell],IAttachmentExecute interface, IAttachmentExecute interface [Windows Shell],ClearClientState method, IAttachmentExecute.ClearClientState, IAttachmentExecute::ClearClientState, shell.IAttachmentExecute_ClearClientState, shell_IAttachmentExecute_clearclientstate, shobjidl_core/IAttachmentExecute::ClearClientState
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
 - IAttachmentExecute.ClearClientState
product: Windows
targetos: Windows
req.lib: 
req.dll: Shdocvw.dll (version 6.0 or later)
req.irql: 
req.product: Outlook Express 6.0
---

# IAttachmentExecute::ClearClientState


## -description


Removes any stored state that is based on the client's GUID. An example might be a setting based on a checked box that indicates a prompt should not be displayed again for a particular file type.


## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




<a href="https://msdn.microsoft.com/d0ee35f7-c23e-450b-8b90-0fb5744263fd">IAttachmentExecute::SetClientGuid</a> must be called before using <b>IAttachmentExecute::ClearClientState</b>.



