---
UID: NF:wintrust.OpenPersonalTrustDBDialog
title: OpenPersonalTrustDBDialog function
author: windows-sdk-content
description: Displays the Certificates dialog box.
old-location: security\openpersonaltrustdbdialog.htm
old-project: SecCrypto
ms.assetid: 25f1d012-0c82-4992-b924-b539d4c6dc5f
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: OpenPersonalTrustDBDialog, OpenPersonalTrustDBDialog function [Security], security.openpersonaltrustdbdialog, wintrust/OpenPersonalTrustDBDialog
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wintrust.h
req.include-header: 
req.redist: 
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
req.typenames: TEB, *PTEB
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wintrust.dll
api_name:
 - OpenPersonalTrustDBDialog
product: Windows
targetos: Windows
req.lib: 
req.dll: Wintrust.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# OpenPersonalTrustDBDialog function


## -description


The <b>OpenPersonalTrustDBDialog</b> function displays the <b>Certificates</b> dialog box.
<div class="alert"><b>Note</b>  This function has no associated header file or import library. You must define the function yourself and use the <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> and <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> functions to dynamically link to Wintrust.dll.</div><div> </div>

## -parameters




### -param hwndParent [in, optional]

The handle of the parent window for the dialog box. If this parameter is <b>NULL</b>, the dialog box has no parent.


## -returns



Returns nonzero if the dialog box was opened successfully or zero otherwise.



