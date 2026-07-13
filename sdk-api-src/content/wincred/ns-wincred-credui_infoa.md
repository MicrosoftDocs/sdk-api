---
UID: NS:wincred._CREDUI_INFOA
title: CREDUI_INFOA (wincred.h)
description: The CREDUI_INFO structure is used to pass information to the CredUIPromptForCredentials function that creates a dialog box used to obtain credentials information. (ANSI)
helpviewer_keywords: ["*PCREDUI_INFOA","CREDUI_INFO","CREDUI_INFO structure [Security]","CREDUI_INFOA","PCREDUI_INFO","PCREDUI_INFO structure pointer [Security]","_cred_credui_info","security.credui_info","wincred/CREDUI_INFO","wincred/PCREDUI_INFO"]
old-location: security\credui_info.htm
tech.root: security
ms.assetid: b21f8a42-3707-409c-b62a-9bbb29137b9b
ms.date: 12/05/2018
ms.keywords: '*PCREDUI_INFOA, CREDUI_INFO, CREDUI_INFO structure [Security], CREDUI_INFOA, PCREDUI_INFO, PCREDUI_INFO structure pointer [Security], _cred_credui_info, security.credui_info, wincred/CREDUI_INFO, wincred/PCREDUI_INFO'
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
targetos: Windows
req.typenames: CREDUI_INFOA, *PCREDUI_INFOA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CREDUI_INFOA
 - wincred/_CREDUI_INFOA
 - PCREDUI_INFOA
 - wincred/PCREDUI_INFOA
 - CREDUI_INFOA
 - wincred/CREDUI_INFOA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinCred.h
api_name:
 - CREDUI_INFO
---

# CREDUI_INFOA structure


## -description

The <b>CREDUI_INFO</b> structure is used to pass information to the 
<a href="/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa">CredUIPromptForCredentials</a> function that creates a dialog box used to obtain credentials information.

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

## -remarks

> [!NOTE]
> The wincred.h header defines CREDUI_INFO as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
