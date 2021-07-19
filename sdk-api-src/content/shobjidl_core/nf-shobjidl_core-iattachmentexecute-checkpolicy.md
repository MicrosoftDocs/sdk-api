---
UID: NF:shobjidl_core.IAttachmentExecute.CheckPolicy
title: IAttachmentExecute::CheckPolicy (shobjidl_core.h)
description: Provides a Boolean test that can be used to make decisions based on the attachment's execution policy.
helpviewer_keywords: ["CheckPolicy","CheckPolicy method [Windows Shell]","CheckPolicy method [Windows Shell]","IAttachmentExecute interface","IAttachmentExecute interface [Windows Shell]","CheckPolicy method","IAttachmentExecute.CheckPolicy","IAttachmentExecute::CheckPolicy","_win32_IAttachmentExecute_CheckPolicy","shell.IAttachmentExecute_CheckPolicy","shobjidl_core/IAttachmentExecute::CheckPolicy"]
old-location: shell\IAttachmentExecute_CheckPolicy.htm
tech.root: shell
ms.assetid: ff6a0aa8-4d14-4074-b084-be117b01c77a
ms.date: 12/05/2018
ms.keywords: CheckPolicy, CheckPolicy method [Windows Shell], CheckPolicy method [Windows Shell],IAttachmentExecute interface, IAttachmentExecute interface [Windows Shell],CheckPolicy method, IAttachmentExecute.CheckPolicy, IAttachmentExecute::CheckPolicy, _win32_IAttachmentExecute_CheckPolicy, shell.IAttachmentExecute_CheckPolicy, shobjidl_core/IAttachmentExecute::CheckPolicy
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAttachmentExecute::CheckPolicy
 - shobjidl_core/IAttachmentExecute::CheckPolicy
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shdocvw.dll
api_name:
 - IAttachmentExecute.CheckPolicy
---

# IAttachmentExecute::CheckPolicy


## -description

Provides a Boolean test that can be used to make decisions based on the attachment's execution policy.



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
<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iattachmentexecute-setfilename">IAttachmentExecute::SetFileName</a>
</li>
<li>
<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iattachmentexecute-setlocalpath">IAttachmentExecute::SetLocalPath</a>
</li>
<li>
<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iattachmentexecute-setreferrer">IAttachmentExecute::SetReferrer</a>
</li>
<li>
<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iattachmentexecute-setsource">IAttachmentExecute::SetSource</a>
</li>
</ul>
The information returned by <b>IAttachmentExecute::CheckPolicy</b> enables an application to modify its UI appropriately for the situation.
			

<b>IAttachmentExecute::CheckPolicy</b> requires the application first to call either <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iattachmentexecute-setfilename">IAttachmentExecute::SetFileName</a> or <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iattachmentexecute-setlocalpath">IAttachmentExecute::SetLocalPath</a>.
