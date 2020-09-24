---
UID: NS:shellapi._NOTIFYICONIDENTIFIER
title: NOTIFYICONIDENTIFIER (shellapi.h)
description: Contains information used by Shell_NotifyIconGetRect to identify the icon for which to retrieve the bounding rectangle.
helpviewer_keywords: ["*PNOTIFYICONIDENTIFIER","NOTIFYICONIDENTIFIER","NOTIFYICONIDENTIFIER structure [Windows Shell]","PNOTIFYICONIDENTIFIER","PNOTIFYICONIDENTIFIER structure pointer [Windows Shell]","_shell_NOTIFYICONIDENTIFIER","shell.NOTIFYICONIDENTIFIER","shellapi/NOTIFYICONIDENTIFIER","shellapi/PNOTIFYICONIDENTIFIER"]
old-location: shell\NOTIFYICONIDENTIFIER.htm
tech.root: shell
ms.assetid: 2fe4ffba-6fe5-4d34-9cb1-f266e4594b8e
ms.date: 12/05/2018
ms.keywords: '*PNOTIFYICONIDENTIFIER, NOTIFYICONIDENTIFIER, NOTIFYICONIDENTIFIER structure [Windows Shell], PNOTIFYICONIDENTIFIER, PNOTIFYICONIDENTIFIER structure pointer [Windows Shell], _shell_NOTIFYICONIDENTIFIER, shell.NOTIFYICONIDENTIFIER, shellapi/NOTIFYICONIDENTIFIER, shellapi/PNOTIFYICONIDENTIFIER'
req.header: shellapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: NOTIFYICONIDENTIFIER, *PNOTIFYICONIDENTIFIER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _NOTIFYICONIDENTIFIER
 - shellapi/_NOTIFYICONIDENTIFIER
 - PNOTIFYICONIDENTIFIER
 - shellapi/PNOTIFYICONIDENTIFIER
 - NOTIFYICONIDENTIFIER
 - shellapi/NOTIFYICONIDENTIFIER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shellapi.h
api_name:
 - NOTIFYICONIDENTIFIER
---

# NOTIFYICONIDENTIFIER structure


## -description

Contains information used by <a href="/windows/desktop/api/shellapi/nf-shellapi-shell_notifyicongetrect">Shell_NotifyIconGetRect</a> to identify the icon for which to retrieve the bounding rectangle.

## -struct-fields

### -field cbSize

Type: <b>DWORD</b>

The size of this structure, in bytes.

### -field hWnd

Type: <b>HWND</b>

A handle to the parent window used by the notification's callback function. For more information, see the <i>hWnd</i> member of the <a href="/windows/desktop/api/shellapi/ns-shellapi-notifyicondataa">NOTIFYICONDATA</a> structure.

### -field uID

Type: <b>UINT</b>

The application-defined identifier of the notification icon. Multiple icons can be associated with a single <i>hWnd</i>, each with their own <i>uID</i>.

### -field guidItem

Type: <b>GUID</b>

A registered GUID that identifies the icon. Use <b>GUID_NULL</b> if the icon is not identified by a GUID.

## -remarks

The icon can be identified to <a href="/windows/desktop/api/shellapi/nf-shellapi-shell_notifyicongetrect">Shell_NotifyIconGetRect</a> through this structure in two ways:
            
                

<ul>
<li><i>guidItem</i> alone (recommended)</li>
<li><i>hWnd</i> plus <i>uID</i></li>
</ul>
If <i>guidItem</i> is not <b>GUID_NULL</b>, <i>hWnd</i> and <i>uID</i> are ignored.