---
UID: NF:cryptuiapi.CryptUIDlgCertMgr
title: CryptUIDlgCertMgr function
author: windows-sdk-content
description: Displays a dialog box that allows the user to manage certificates.
old-location: security\cryptuidlgcertmgr.htm
tech.root: seccrypto
ms.assetid: 8d94694e-1724-42aa-99bb-6ed2c6d3bc0e
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: CryptUIDlgCertMgr, CryptUIDlgCertMgr function [Security], cryptuiapi/CryptUIDlgCertMgr, security.cryptuidlgcertmgr
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CryptUIDlgCertMgr function


## -description


The <b>CryptUIDlgCertMgr</b> function displays a dialog box that allows the user to manage certificates.


## -parameters




### -param pCryptUICertMgr [in]

A pointer to a <a href="https://msdn.microsoft.com/e6c24d16-0ae2-443c-8971-2d7da3aae963">CRYPTUI_CERT_MGR_STRUCT</a> structure that contains information about how to create the dialog box.


## -returns



The return value is <b>TRUE</b> if the function succeeds; otherwise, <b>FALSE.</b>



