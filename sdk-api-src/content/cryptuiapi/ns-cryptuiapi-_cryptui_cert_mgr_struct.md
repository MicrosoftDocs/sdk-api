---
UID: NS:cryptuiapi._CRYPTUI_CERT_MGR_STRUCT
title: "_CRYPTUI_CERT_MGR_STRUCT"
author: windows-sdk-content
description: Contains information about a certificate manager dialog box.
old-location: security\cryptui_cert_mgr_struct.htm
tech.root: seccrypto
ms.assetid: e6c24d16-0ae2-443c-8971-2d7da3aae963
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: "*PCRYPTUI_CERT_MGR_STRUCT, CRYPTUI_CERT_MGR_STRUCT, CRYPTUI_CERT_MGR_STRUCT structure [Security], PCRYPTUI_CERT_MGR_STRUCT, PCRYPTUI_CERT_MGR_STRUCT structure pointer [Security], _CRYPTUI_CERT_MGR_STRUCT, cryptuiapi/CRYPTUI_CERT_MGR_STRUCT, cryptuiapi/PCRYPTUI_CERT_MGR_STRUCT, security.cryptui_cert_mgr_struct"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: cryptuiapi.h
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
 - Cryptuiapi.h
api_name:
 - CRYPTUI_CERT_MGR_STRUCT
product: Windows
targetos: Windows
req.typenames: CRYPTUI_CERT_MGR_STRUCT, *PCRYPTUI_CERT_MGR_STRUCT
req.redist: 
---

# _CRYPTUI_CERT_MGR_STRUCT structure


## -description


The <b>CRYPTUI_CERT_MGR_STRUCT</b> structure contains information about a certificate manager dialog box.


## -struct-fields




### -field dwSize

The size, in bytes, of the structure. This value must be set to <code>sizeof(CRYPTUI_CERT_MGR_STRUCT)</code>.


### -field hwndParent

Handle of the parent window of the dialog box.


### -field dwFlags

Reserved. This value must be set to zero.


### -field pwszTitle

Title of the dialog box.


### -field pszInitUsageOID

Enhanced key usage <a href="https://msdn.microsoft.com/en-us/library/ms721599(v=VS.85).aspx">object identifier</a> (OID) of the certificates that will initially appear in the dialog box. The default value is <b>NULL</b>, which displays all certificates.

