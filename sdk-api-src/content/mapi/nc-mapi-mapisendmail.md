---
UID: NC:mapi.MAPISENDMAIL
title: MAPISENDMAIL (mapi.h)
description: Sends an ANSI message.
helpviewer_keywords: ["MAPISendMail","MAPISendMail callback","MAPISendMail callback function","mapi.mapisendmail","mapi/MAPISendMail"]
old-location: mapi\mapisendmail.htm
tech.root: mapi
ms.assetid: 1d7da0f2-b736-401e-86bd-fc4375ccc0d1
ms.date: 12/05/2018
ms.keywords: MAPISendMail, MAPISendMail callback, MAPISendMail callback function, mapi.mapisendmail, mapi/MAPISendMail
req.header: mapi.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MAPISENDMAIL
 - mapi/MAPISENDMAIL
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Mapi.h
api_name:
 - MAPISendMail
---

# MAPISENDMAIL callback function


## -description

<p class="CCE_Message">[<b>MAPISendMail</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/previous-versions/windows/desktop/api/mapi/nc-mapi-mapisendmailw">MAPISendMailW</a>.
]

Sends an ANSI message.

<b>On Windows 8 and later:  </b>Call <a href="/previous-versions/windows/desktop/api/mapi/nc-mapi-mapisendmailw">MAPISendMailW</a> to send a message.

<b>On Windows 7 and earlier:  </b>Use <a href="/previous-versions/windows/desktop/api/mapiunicodehelp/nf-mapiunicodehelp-mapisendmailhelper">MAPISendMailHelper</a> to send a message.

## -parameters

### -param lhSession [in]

Type: <b>LHANDLE</b>

For more information, see the <a href="/previous-versions/windows/desktop/api/mapi/nc-mapi-mapisendmailw">MAPISendMailW</a> function.

### -param ulUIParam [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">ULONG_PTR</a></b>

For more information, see the <a href="/previous-versions/windows/desktop/api/mapi/nc-mapi-mapisendmailw">MAPISendMailW</a> function.

### -param lpMessage [in]

Type: <b><a href="/previous-versions/windows/desktop/api/mapi/ns-mapi-mapimessage">lpMapiMessage</a></b>

For more information, see the <a href="/previous-versions/windows/desktop/api/mapi/nc-mapi-mapisendmailw">MAPISendMailW</a> function.

### -param flFlags [in]

Type: <b>FLAGS</b>

For more information, see the <a href="/previous-versions/windows/desktop/api/mapi/nc-mapi-mapisendmailw">MAPISendMailW</a> function.

### -param ulReserved

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">ULONG</a></b>

For more information, see the <a href="/previous-versions/windows/desktop/api/mapi/nc-mapi-mapisendmailw">MAPISendMailW</a> function.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">ULONG</a></b>

For more information, see the <a href="/previous-versions/windows/desktop/api/mapi/nc-mapi-mapisendmailw">MAPISendMailW</a> function.

## -see-also

<a href="/previous-versions/windows/desktop/api/mapi/nc-mapi-mapilogon">MAPILogon</a>



<a href="/previous-versions/windows/desktop/api/mapi/nc-mapi-mapisenddocuments">MAPISendDocuments</a>



<a href="/previous-versions/windows/desktop/api/mapiunicodehelp/nf-mapiunicodehelp-mapisendmailhelper">MAPISendMailHelper</a>



<a href="/previous-versions/windows/desktop/api/mapi/nc-mapi-mapisendmailw">MAPISendMailW</a>



<a href="/previous-versions/windows/desktop/api/mapi/ns-mapi-mapimessage">MapiMessage</a>



<a href="/previous-versions/windows/desktop/api/mapi/ns-mapi-mapirecipdesc">MapiRecipDesc</a>



<a href="/previous-versions/dd296734(v=vs.85)">Simple MAPI</a>