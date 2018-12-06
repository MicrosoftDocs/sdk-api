---
UID: NF:shobjidl_core.IAttachmentExecute.SetLocalPath
title: IAttachmentExecute::SetLocalPath
author: windows-sdk-content
description: Sets and stores the path to the file.
old-location: shell\IAttachmentExecute_SetLocalPath.htm
tech.root: shell
ms.assetid: 763ce5a7-bbad-4dd8-a416-86a96f466510
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IAttachmentExecute interface [Windows Shell],SetLocalPath method, IAttachmentExecute.SetLocalPath, IAttachmentExecute::SetLocalPath, SetLocalPath, SetLocalPath method [Windows Shell], SetLocalPath method [Windows Shell],IAttachmentExecute interface, _win32_IAttachmentExecute_SetLocalPath, shell.IAttachmentExecute_SetLocalPath, shobjidl_core/IAttachmentExecute::SetLocalPath
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
 - IAttachmentExecute.SetLocalPath
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAttachmentExecute::SetLocalPath


## -description


Sets and stores the path to the file.


## -parameters




### -param pszLocalPath [in]

Type: <b>LPCWSTR</b>

A pointer to a string that contains the local path where the attachment file is to be stored.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Calling <b>IAttachmentExecute::SetLocalPath</b> is required.

When the attachment is approved for execution by the user (either through policy or prompt), the path specified by this method is used. If only <a href="https://msdn.microsoft.com/52dc823f-4429-4c1f-8906-9e4ee3f8158e">IAttachmentExecute::SetFileName</a> was called before calling <a href="https://msdn.microsoft.com/ff6a0aa8-4d14-4074-b084-be117b01c77a">IAttachmentExecute::CheckPolicy</a> and <a href="https://msdn.microsoft.com/01c01abf-df7a-411b-979b-ddd8da569f91">IAttachmentExecute::Prompt</a>, that trust could be revoked if the assumed local path was different from that set by <b>IAttachmentExecute::SetLocalPath</b>. Trust can be granted by various Zone APIs, antivirus services, file type information, policies as well as other system trust providers.

<b>IAttachmentExecute::SetLocalPath</b> must be called before calling <a href="https://msdn.microsoft.com/80cbbb6c-c6f1-4937-9c1e-4de57aee748c">IAttachmentExecute::Execute</a>.




## -see-also




<a href="https://msdn.microsoft.com/2ebc3197-aa28-446e-8452-8ff71764fa9d">IAttachmentExecute</a>



<a href="https://msdn.microsoft.com/52dc823f-4429-4c1f-8906-9e4ee3f8158e">IAttachmentExecute::SetFileName</a>
 

 

