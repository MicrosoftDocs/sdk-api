---
UID: NE:faxcomex.FAX_SMTP_AUTHENTICATION_TYPE_ENUM
title: FAX_SMTP_AUTHENTICATION_TYPE_ENUM (faxcomex.h)
description: The FAX_SMTP_AUTHENTICATION_TYPE_ENUM enumeration defines the configuration options for delivery receipts sent through email.
helpviewer_keywords: ["FAX_SMTP_AUTHENTICATION_TYPE_ENUM","FAX_SMTP_AUTHENTICATION_TYPE_ENUM enumeration [Fax Service]","_mfax_fax_smtp_authentication_type_enum","fax._mfax_fax_smtp_authentication_type_enum","faxcomex/FAX_SMTP_AUTHENTICATION_TYPE_ENUM","faxcomex/fsatANONYMOUS","faxcomex/fsatBASIC","faxcomex/fsatNTLM","fsatANONYMOUS","fsatBASIC","fsatNTLM"]
old-location: fax\_mfax_fax_smtp_authentication_type_enum.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_1vot.htm
ms.date: 12/05/2018
ms.keywords: FAX_SMTP_AUTHENTICATION_TYPE_ENUM, FAX_SMTP_AUTHENTICATION_TYPE_ENUM enumeration [Fax Service], _mfax_fax_smtp_authentication_type_enum, fax._mfax_fax_smtp_authentication_type_enum, faxcomex/FAX_SMTP_AUTHENTICATION_TYPE_ENUM, faxcomex/fsatANONYMOUS, faxcomex/fsatBASIC, faxcomex/fsatNTLM, fsatANONYMOUS, fsatBASIC, fsatNTLM
req.header: faxcomex.h
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
req.typenames: FAX_SMTP_AUTHENTICATION_TYPE_ENUM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FAX_SMTP_AUTHENTICATION_TYPE_ENUM
 - faxcomex/FAX_SMTP_AUTHENTICATION_TYPE_ENUM
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - FaxComex.h
api_name:
 - FAX_SMTP_AUTHENTICATION_TYPE_ENUM
---

# FAX_SMTP_AUTHENTICATION_TYPE_ENUM enumeration


## -description

The <b>FAX_SMTP_AUTHENTICATION_TYPE_ENUM</b> enumeration defines the configuration options for delivery receipts sent through email.

## -enum-fields

### -field fsatANONYMOUS:0

The server sends fax transmission receipts using a nonauthenticated SMTP protocol.

### -field fsatBASIC

The server sends fax transmission receipts using a basic (plain text) authenticated SMTP protocol.

### -field fsatNTLM

The server sends fax transmission receipts using an NTLM-authenticated SMTP protocol.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxreceiptoptions-authenticationtype-vb">IFaxReceiptOptions::get_AuthenticationType</a>
