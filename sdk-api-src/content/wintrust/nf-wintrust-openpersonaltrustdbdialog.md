---
UID: NF:wintrust.OpenPersonalTrustDBDialog
title: OpenPersonalTrustDBDialog function (wintrust.h)
description: Displays the Certificates dialog box. (OpenPersonalTrustDBDialog)
helpviewer_keywords: ["OpenPersonalTrustDBDialog","OpenPersonalTrustDBDialog function [Security]","security.openpersonaltrustdbdialog","wintrust/OpenPersonalTrustDBDialog"]
old-location: security\openpersonaltrustdbdialog.htm
tech.root: security
ms.assetid: 25f1d012-0c82-4992-b924-b539d4c6dc5f
ms.date: 12/05/2018
ms.keywords: OpenPersonalTrustDBDialog, OpenPersonalTrustDBDialog function [Security], security.openpersonaltrustdbdialog, wintrust/OpenPersonalTrustDBDialog
req.header: wintrust.h
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
req.dll: Wintrust.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - OpenPersonalTrustDBDialog
 - wintrust/OpenPersonalTrustDBDialog
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wintrust.dll
api_name:
 - OpenPersonalTrustDBDialog
---

# OpenPersonalTrustDBDialog function


## -description

The <b>OpenPersonalTrustDBDialog</b> function displays the <b>Certificates</b> dialog box.
<div class="alert"><b>Note</b>  This function has no associated header file or import library. You must define the function yourself and use the <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> and <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> functions to dynamically link to Wintrust.dll.</div><div> </div>

## -parameters

### -param hwndParent [in, optional]

The handle of the parent window for the dialog box. If this parameter is <b>NULL</b>, the dialog box has no parent.

## -returns

Returns nonzero if the dialog box was opened successfully or zero otherwise.
