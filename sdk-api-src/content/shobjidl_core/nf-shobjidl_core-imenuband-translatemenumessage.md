---
UID: NF:shobjidl_core.IMenuBand.TranslateMenuMessage
title: IMenuBand::TranslateMenuMessage
author: windows-sdk-content
description: Translates a message for a Component Object Model (COM) object.
old-location: shell\IMenuBand_TranslateMenuMessage.htm
old-project: shell
ms.assetid: 5ee1f64f-ca8b-4f50-bbab-24ff1216708c
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: IMenuBand interface [Windows Shell],TranslateMenuMessage method, IMenuBand.TranslateMenuMessage, IMenuBand::TranslateMenuMessage, TranslateMenuMessage, TranslateMenuMessage method [Windows Shell], TranslateMenuMessage method [Windows Shell],IMenuBand interface, _shell_IMenuBand_TranslateMenuMessage, shell.IMenuBand_TranslateMenuMessage, shobjidl_core/IMenuBand::TranslateMenuMessage
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
 - Shell32.dll
api_name:
 - IMenuBand.TranslateMenuMessage
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll
req.irql: 
req.product: Outlook Express 6.0
---

# IMenuBand::TranslateMenuMessage


## -description


Translates a message for a Component Object Model (COM) object.


## -parameters




### -param pmsg [in, out]

Type: <b><a href="https://msdn.microsoft.com/fee176ba-ad07-4145-ab4d-1b8c335fd100">MSG</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/fee176ba-ad07-4145-ab4d-1b8c335fd100">MSG</a> structure that contains the incoming message.


### -param plRet [out]

Type: <b>LRESULT*</b>

A pointer to the translated message.


## -returns



Type: <b>HRESULT</b>

This method can return one of these values.

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
The message was handled and should be deleted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The message was not handled. In this case, *plRet is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



Typically, <a href="https://msdn.microsoft.com/d30a456c-7c09-4250-8509-353c54d017b9">IMenuBand::IsMenuMessage</a> is called before this method. The parent window proc, not the message pump, must call <b>IMenuBand::TranslateMenuMessage</b> for every message.

This method can change the values of <i>pmsg</i>. If so, the changes should be forwarded on.

This method is required because some modal message pumps do not allow a call to a custom translation method.



