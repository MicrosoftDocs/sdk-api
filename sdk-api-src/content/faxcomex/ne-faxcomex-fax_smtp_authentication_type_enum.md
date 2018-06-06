---
UID: NE:faxcomex.FAX_SMTP_AUTHENTICATION_TYPE_ENUM
title: FAX_SMTP_AUTHENTICATION_TYPE_ENUM
author: windows-sdk-content
description: The FAX_SMTP_AUTHENTICATION_TYPE_ENUM enumeration defines the configuration options for delivery receipts sent through email.
old-location: fax\_mfax_fax_smtp_authentication_type_enum.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_1vot.htm
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: FAX_SMTP_AUTHENTICATION_TYPE_ENUM, FAX_SMTP_AUTHENTICATION_TYPE_ENUM enumeration [Fax Service], _mfax_fax_smtp_authentication_type_enum, fax._mfax_fax_smtp_authentication_type_enum, faxcomex/FAX_SMTP_AUTHENTICATION_TYPE_ENUM, faxcomex/fsatANONYMOUS, faxcomex/fsatBASIC, faxcomex/fsatNTLM, fsatANONYMOUS, fsatBASIC, fsatNTLM
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: FAX_SMTP_AUTHENTICATION_TYPE_ENUM
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - FaxComex.h
api_name:
 - FAX_SMTP_AUTHENTICATION_TYPE_ENUM
product: Windows
targetos: Windows
req.lib: 
req.dll: Faxcom.dll
req.irql: 
req.product: Internet Explorer 5
---

# FAX_SMTP_AUTHENTICATION_TYPE_ENUM enumeration


## -description


The <b>FAX_SMTP_AUTHENTICATION_TYPE_ENUM</b> enumeration defines the configuration options for delivery receipts sent through email.


## -enum-fields




### -field fsatANONYMOUS

The server sends fax transmission receipts using a nonauthenticated SMTP protocol. 


### -field fsatBASIC

The server sends fax transmission receipts using a basic (plain text) authenticated SMTP protocol. 


### -field fsatNTLM

The server sends fax transmission receipts using an NTLM-authenticated SMTP protocol. 


## -see-also




<a href="https://msdn.microsoft.com/1624ad8c-07ca-4ab1-970c-fb0624903b81">IFaxReceiptOptions::get_AuthenticationType</a>
 

 

