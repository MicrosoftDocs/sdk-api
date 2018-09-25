---
UID: NS:wincred._CREDUI_INFOW
title: "_CREDUI_INFOW"
author: windows-sdk-content
description: The CREDUI_INFO structure is used to pass information to the CredUIPromptForCredentials function that creates a dialog box used to obtain credentials information.
old-location: security\credui_info.htm
tech.root: secauthn
ms.assetid: b21f8a42-3707-409c-b62a-9bbb29137b9b
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: "*PCREDUI_INFOW, CREDUI_INFO, CREDUI_INFO structure [Security], CREDUI_INFOW, PCREDUI_INFO, PCREDUI_INFO structure pointer [Security], _CREDUI_INFOW, _cred_credui_info, security.credui_info, wincred/CREDUI_INFO, wincred/PCREDUI_INFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wincred.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinCred.h
api_name:
 - CREDUI_INFO
product: Windows
targetos: Windows
req.typenames: CREDUI_INFOW, *PCREDUI_INFOW
req.redist: 
---

# _CREDUI_INFOW structure


## -description


The <b>CREDUI_INFO</b> structure is used to pass information to the 
<a href="https://msdn.microsoft.com/97a8e750-3e63-4e6f-a875-1e5c49c30dd4">CredUIPromptForCredentials</a> function that creates a dialog box used to obtain credentials information.


## -struct-fields




### -field cbSize

Set to the size of the CREDUI_INFO structure.


### -field hwndParent

Specifies the handle to the parent window of the dialog box. The dialog box is modal with respect to the parent window. If this member is <b>NULL</b>, the desktop is the parent window of the dialog box.


### -field pszMessageText

Pointer to a string containing a brief message to display in the dialog box. The length of this string should not exceed CREDUI_MAX_MESSAGE_LENGTH.


### -field pszCaptionText

Pointer to a string containing the title for the dialog box. The length of this string should not exceed CREDUI_MAX_CAPTION_LENGTH.


### -field hbmBanner

Bitmap to display in the dialog box. If this member is <b>NULL</b>, a default bitmap is used. The bitmap size is limited to 320x60 pixels.

