---
UID: NF:shobjidl_core.IAttachmentExecute.Save
title: IAttachmentExecute::Save
author: windows-sdk-content
description: Saves the attachment.
old-location: shell\IAttachmentExecute_Save.htm
old-project: shell
ms.assetid: 25661942-f38b-42d6-981b-4a3f4d083f6c
ms.author: windowssdkdev
ms.date: 07/20/2018
ms.keywords: IAttachmentExecute interface [Windows Shell],Save method, IAttachmentExecute.Save, IAttachmentExecute::Save, Save, Save method [Windows Shell], Save method [Windows Shell],IAttachmentExecute interface, _win32_IAttachmentExecute_Save, shell.IAttachmentExecute_Save, shobjidl_core/IAttachmentExecute::Save
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
 - IAttachmentExecute.Save
product: Windows
targetos: Windows
req.lib: 
req.dll: Shdocvw.dll (version 6.0 or later)
req.irql: 
req.product: Outlook Express 6.0
---

# IAttachmentExecute::Save


## -description


Saves the attachment.


## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Before calling <b>IAttachmentExecute::Save</b>, you must call <a href="https://msdn.microsoft.com/763ce5a7-bbad-4dd8-a416-86a96f466510">IAttachmentExecute::SetLocalPath</a> with a valid path. The file should be copied to that local path before <b>IAttachmentExecute::Save</b> is called.

<b>IAttachmentExecute::Save</b> should always be called if the local path declared in <a href="https://msdn.microsoft.com/763ce5a7-bbad-4dd8-a416-86a96f466510">IAttachmentExecute::SetLocalPath</a> is not the path of a temporary directory.

<b>IAttachmentExecute::Save</b> may run virus scanners or other trust services to validate the file before saving it. Note that these services can delete or alter the file.

<b>IAttachmentExecute::Save</b> may attach <a href="https://msdn.microsoft.com/ff6a0aa8-4d14-4074-b084-be117b01c77a">evidence</a> to the local path in its NTFS alternate data stream (ADS).




## -see-also




<a href="https://msdn.microsoft.com/2ebc3197-aa28-446e-8452-8ff71764fa9d">IAttachmentExecute</a>



<a href="https://msdn.microsoft.com/6d5b2d02-98ee-4e46-826f-fa073ecff5c4">IAttachmentExecute::SaveWithUI</a>
 

 

