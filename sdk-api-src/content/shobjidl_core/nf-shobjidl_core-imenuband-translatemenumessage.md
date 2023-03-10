---
UID: NF:shobjidl_core.IMenuBand.TranslateMenuMessage
title: IMenuBand::TranslateMenuMessage (shobjidl_core.h)
description: Translates a message for a Component Object Model (COM) object.
helpviewer_keywords: ["IMenuBand interface [Windows Shell]","TranslateMenuMessage method","IMenuBand.TranslateMenuMessage","IMenuBand::TranslateMenuMessage","TranslateMenuMessage","TranslateMenuMessage method [Windows Shell]","TranslateMenuMessage method [Windows Shell]","IMenuBand interface","_shell_IMenuBand_TranslateMenuMessage","shell.IMenuBand_TranslateMenuMessage","shobjidl_core/IMenuBand::TranslateMenuMessage"]
old-location: shell\IMenuBand_TranslateMenuMessage.htm
tech.root: shell
ms.assetid: 5ee1f64f-ca8b-4f50-bbab-24ff1216708c
ms.date: 12/05/2018
ms.keywords: IMenuBand interface [Windows Shell],TranslateMenuMessage method, IMenuBand.TranslateMenuMessage, IMenuBand::TranslateMenuMessage, TranslateMenuMessage, TranslateMenuMessage method [Windows Shell], TranslateMenuMessage method [Windows Shell],IMenuBand interface, _shell_IMenuBand_TranslateMenuMessage, shell.IMenuBand_TranslateMenuMessage, shobjidl_core/IMenuBand::TranslateMenuMessage
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
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
req.lib: 
req.dll: Shell32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMenuBand::TranslateMenuMessage
 - shobjidl_core/IMenuBand::TranslateMenuMessage
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IMenuBand.TranslateMenuMessage
---

# IMenuBand::TranslateMenuMessage


## -description

Translates a message for a Component Object Model (COM) object.

## -parameters

### -param pmsg [in, out]

Type: <b><a href="/windows/desktop/api/winuser/ns-winuser-msg">MSG</a>*</b>

A pointer to an <a href="/windows/desktop/api/winuser/ns-winuser-msg">MSG</a> structure that contains the incoming message.

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

Typically, <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenuband-ismenumessage">IMenuBand::IsMenuMessage</a> is called before this method. The parent window proc, not the message pump, must call <b>IMenuBand::TranslateMenuMessage</b> for every message.

This method can change the values of <i>pmsg</i>. If so, the changes should be forwarded on.

This method is required because some modal message pumps do not allow a call to a custom translation method.