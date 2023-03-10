---
UID: NF:photoacquire.IUserInputString.GetPrompt
title: IUserInputString::GetPrompt (photoacquire.h)
description: The GetPrompt method retrieves the title of a prompt if the prompt is a modal dialog box.
helpviewer_keywords: ["GetPrompt","GetPrompt method [Picture Acquisition]","GetPrompt method [Picture Acquisition]","IUserInputString interface","IUserInputString interface [Picture Acquisition]","GetPrompt method","IUserInputString.GetPrompt","IUserInputString::GetPrompt","IUserInputStringGetPrompt","photoacquire/IUserInputString::GetPrompt","picacq.iuserinputstring_getprompt"]
old-location: picacq\iuserinputstring_getprompt.htm
tech.root: picacq
ms.assetid: f2fdb18d-5af8-45c8-8f92-7fc8c836082d
ms.date: 12/05/2018
ms.keywords: GetPrompt, GetPrompt method [Picture Acquisition], GetPrompt method [Picture Acquisition],IUserInputString interface, IUserInputString interface [Picture Acquisition],GetPrompt method, IUserInputString.GetPrompt, IUserInputString::GetPrompt, IUserInputStringGetPrompt, photoacquire/IUserInputString::GetPrompt, picacq.iuserinputstring_getprompt
req.header: photoacquire.h
req.include-header: 
req.target-type: Windows
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
req.lib: PhotoAcquireUID.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUserInputString::GetPrompt
 - photoacquire/IUserInputString::GetPrompt
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - PhotoAcquireUID.lib
 - PhotoAcquireUID.dll
api_name:
 - IUserInputString.GetPrompt
---

# IUserInputString::GetPrompt


## -description

The <code>GetPrompt</code> method retrieves the title of a prompt if the prompt is a modal dialog box.

## -parameters

### -param pbstrPromptTitle [out]

Pointer to a string containing the title of the prompt.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A <b>NULL</b> pointer was passed where a non-<b>NULL</b> pointer is expected.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/photoacquire/nn-photoacquire-iuserinputstring">IUserInputString Interface</a>