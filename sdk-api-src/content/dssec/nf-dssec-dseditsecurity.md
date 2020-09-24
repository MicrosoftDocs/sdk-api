---
UID: NF:dssec.DSEditSecurity
title: DSEditSecurity function (dssec.h)
description: Displays a modal dialog box for editing security on a Directory Services (DS) object.
helpviewer_keywords: ["DSEditSecurity","DSEditSecurity function [Security]","dssec/DSEditSecurity","security.dseditsecurity"]
old-location: security\dseditsecurity.htm
tech.root: security
ms.assetid: e440e696-37a5-4853-b205-a4701b2c9beb
ms.date: 12/05/2018
ms.keywords: DSEditSecurity, DSEditSecurity function [Security], dssec/DSEditSecurity, security.dseditsecurity
req.header: dssec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: DSSec.lib
req.dll: DSSec.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DSEditSecurity
 - dssec/DSEditSecurity
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - DSSec.dll
api_name:
 - DSEditSecurity
---

# DSEditSecurity function


## -description

The <b>DSEditSecurity</b> function displays a modal dialog box for editing security on a Directory Services (DS) object.

## -parameters

### -param hwndOwner [in]

The dialog box owner window.

### -param pwszObjectPath [in]

The full Active Directory Services (ADS) path of the DS object.

### -param pwszObjectClass [in, optional]

The class of the object.

### -param dwFlags [in]

The combination of DSSI_* flags.

### -param pwszCaption [in, optional]

The dialog box caption.

### -param pfnReadSD [in, optional]

The function for reading the object.

### -param pfnWriteSD [in, optional]

The function for writing the object.

### -param lpContext [in]

The context passed into the read or write functions in the <i>pfnReadSD</i> and <i>pfnWriteSD</i> parameters.

## -returns

If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.