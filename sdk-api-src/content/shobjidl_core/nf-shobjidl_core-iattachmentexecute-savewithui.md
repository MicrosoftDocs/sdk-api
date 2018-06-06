---
UID: NF:shobjidl_core.IAttachmentExecute.SaveWithUI
title: IAttachmentExecute::SaveWithUI
author: windows-sdk-content
description: Presents the user with explanatory error UI if the save action fails.
old-location: shell\IAttachmentExecute_SaveWithUI.htm
old-project: shell
ms.assetid: 6d5b2d02-98ee-4e46-826f-fa073ecff5c4
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IAttachmentExecute interface [Windows Shell],SaveWithUI method, IAttachmentExecute.SaveWithUI, IAttachmentExecute::SaveWithUI, SaveWithUI, SaveWithUI method [Windows Shell], SaveWithUI method [Windows Shell],IAttachmentExecute interface, shell.IAttachmentExecute_SaveWithUI, shell_IAttachmentExecute_savewithui, shobjidl_core/IAttachmentExecute::SaveWithUI
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
 - IAttachmentExecute.SaveWithUI
product: Windows
targetos: Windows
req.lib: 
req.dll: Shdocvw.dll (version 6.0 or later)
req.irql: 
req.product: Outlook Express 6.0
---

# IAttachmentExecute::SaveWithUI


## -description


Presents the user with explanatory error UI if the save action fails.


## -parameters




### -param hwnd [in]

Type: <b>HWND</b>

The handle of the parent window.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<b>IAttachmentExecute::SaveWithUI</b> does not call <a href="https://msdn.microsoft.com/01c01abf-df7a-411b-979b-ddd8da569f91">IAttachmentExecute::Prompt</a>.

Before calling <b>IAttachmentExecute::SaveWithUI</b>, you must call <a href="https://msdn.microsoft.com/763ce5a7-bbad-4dd8-a416-86a96f466510">IAttachmentExecute::SetLocalPath</a> with a valid path. The file is copied to that local path before <b>IAttachmentExecute::SaveWithUI</b> is called.

<b>IAttachmentExecute::SaveWithUI</b> may run virus scanners or other trust services to validate the file before saving it. Note that these services can delete or alter the file.

<b>IAttachmentExecute::SaveWithUI</b> may attach <a href="https://msdn.microsoft.com/ff6a0aa8-4d14-4074-b084-be117b01c77a">evidence</a> to the local path in its NTFS alternate data stream (ADS).




## -see-also




<a href="https://msdn.microsoft.com/2ebc3197-aa28-446e-8452-8ff71764fa9d">IAttachmentExecute</a>



<a href="https://msdn.microsoft.com/25661942-f38b-42d6-981b-4a3f4d083f6c">IAttachmentExecute::Save</a>
 

 

