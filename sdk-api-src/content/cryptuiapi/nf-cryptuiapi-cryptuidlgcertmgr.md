---
UID: NF:cryptuiapi.CryptUIDlgCertMgr
title: CryptUIDlgCertMgr function (cryptuiapi.h)
description: Displays a dialog box that allows the user to manage certificates.
helpviewer_keywords: ["CryptUIDlgCertMgr","CryptUIDlgCertMgr function [Security]","cryptuiapi/CryptUIDlgCertMgr","security.cryptuidlgcertmgr"]
old-location: security\cryptuidlgcertmgr.htm
tech.root: security
ms.assetid: 8d94694e-1724-42aa-99bb-6ed2c6d3bc0e
ms.date: 12/05/2018
ms.keywords: CryptUIDlgCertMgr, CryptUIDlgCertMgr function [Security], cryptuiapi/CryptUIDlgCertMgr, security.cryptuidlgcertmgr
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
req.lib: Cryptui.lib
req.dll: Cryptui.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CryptUIDlgCertMgr
 - cryptuiapi/CryptUIDlgCertMgr
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Cryptui.dll
 - Ext-MS-Win-security-cryptui-l1-1-0.dll
 - ext-ms-win-security-cryptui-l1-1-1.dll
 - CertCredProviderOneCore.dll
api_name:
 - CryptUIDlgCertMgr
---

# CryptUIDlgCertMgr function


## -description

The <b>CryptUIDlgCertMgr</b> function displays a dialog box that allows the user to manage certificates.

## -parameters

### -param pCryptUICertMgr [in]

A pointer to a <a href="/windows/desktop/api/cryptuiapi/ns-cryptuiapi-cryptui_cert_mgr_struct">CRYPTUI_CERT_MGR_STRUCT</a> structure that contains information about how to create the dialog box.

## -returns

The return value is <b>TRUE</b> if the function succeeds; otherwise, <b>FALSE.</b>