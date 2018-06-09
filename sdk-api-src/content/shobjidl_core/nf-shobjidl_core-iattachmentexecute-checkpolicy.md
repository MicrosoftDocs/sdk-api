---
UID: NF:shobjidl_core.IAttachmentExecute.CheckPolicy
title: IAttachmentExecute::CheckPolicy
author: windows-sdk-content
description: Provides a Boolean test that can be used to make decisions based on the attachment's execution policy.
old-location: shell\IAttachmentExecute_CheckPolicy.htm
old-project: shell
ms.assetid: ff6a0aa8-4d14-4074-b084-be117b01c77a
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: CheckPolicy, CheckPolicy method [Windows Shell], CheckPolicy method [Windows Shell],IAttachmentExecute interface, IAttachmentExecute interface [Windows Shell],CheckPolicy method, IAttachmentExecute.CheckPolicy, IAttachmentExecute::CheckPolicy, _win32_IAttachmentExecute_CheckPolicy, shell.IAttachmentExecute_CheckPolicy, shobjidl_core/IAttachmentExecute::CheckPolicy
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
 - IAttachmentExecute.CheckPolicy
product: Windows
targetos: Windows
req.lib: 
req.dll: Shdocvw.dll (version 6.0 or later)
req.irql: 
req.product: Outlook Express 6.0
---

# IAttachmentExecute::CheckPolicy


## -description


Provides a Boolean test that can be used to make decisions based on the attachment's execution policy.


## -parameters






## -returns



Type: <b>HRESULT</b>

Returns one of the following values.
                    

<table class="clsStd">
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>S_OK</td>
<td>Enable</td>
</tr>
<tr>
<td>S_FALSE</td>
<td>Prompt</td>
</tr>
<tr>
<td>Any other failure code</td>
<td>Disable</td>
</tr>
</table>
 




## -remarks



<b>IAttachmentExecute::CheckPolicy</b> examines a set of properties known collectively as <i>evidence</i>. Anything used to determine trust level is considered evidence. These properties are set using the following methods.

				

<ul>
<li>
<a href="https://msdn.microsoft.com/52dc823f-4429-4c1f-8906-9e4ee3f8158e">IAttachmentExecute::SetFileName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/763ce5a7-bbad-4dd8-a416-86a96f466510">IAttachmentExecute::SetLocalPath</a>
</li>
<li>
<a href="https://msdn.microsoft.com/d7ee869a-2afe-4d98-a0bb-d80e57425079">IAttachmentExecute::SetReferrer</a>
</li>
<li>
<a href="https://msdn.microsoft.com/6545252b-1c43-4d62-9784-b63688ef9fdc">IAttachmentExecute::SetSource</a>
</li>
</ul>


				The information returned by <b>IAttachmentExecute::CheckPolicy</b> enables an application to modify its UI appropriately for the situation.
			

<b>IAttachmentExecute::CheckPolicy</b> requires the application first to call either <a href="https://msdn.microsoft.com/52dc823f-4429-4c1f-8906-9e4ee3f8158e">IAttachmentExecute::SetFileName</a> or <a href="https://msdn.microsoft.com/763ce5a7-bbad-4dd8-a416-86a96f466510">IAttachmentExecute::SetLocalPath</a>.



