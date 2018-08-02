---
UID: NS:wsman._WSMAN_CERTIFICATE_DETAILS
title: "_WSMAN_CERTIFICATE_DETAILS"
author: windows-sdk-content
description: Stores client information for an inbound request that was sent with a client certificate.
old-location: winrm\wsman_certificate_details.htm
old-project: WinRM
ms.assetid: 82b723fd-c9bb-4ddd-bd2a-4b6d1186846b
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: WSMAN_CERTIFICATE_DETAILS, WSMAN_CERTIFICATE_DETAILS structure [Windows Remote Management], _WSMAN_CERTIFICATE_DETAILS, winrm.wsman_certificate_details, wsman/WSMAN_CERTIFICATE_DETAILS
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wsman.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
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
req.typenames: WSMAN_CERTIFICATE_DETAILS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wsman.h
api_name:
 - WSMAN_CERTIFICATE_DETAILS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _WSMAN_CERTIFICATE_DETAILS structure


## -description


Stores client information for an inbound request that was sent with a client certificate.  The individual fields represent the fields within the client certificate.


## -struct-fields




### -field subject

Specifies the subject that is identified by the certificate.


### -field issuerName

Specifies the name of the issuer of the certificate.


### -field issuerThumbprint

Specifies the thumbprint of the issuer.


### -field subjectName

Specifies the subject name of the issuer.

