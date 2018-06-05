---
UID: NF:edpwin32.ProtectFileToEnterpriseIdentity
title: ProtectFileToEnterpriseIdentity function
author: windows-sdk-content
description: Protects the data in a file to an enterprise identity, so that only users who are associated with that enterprise identity can access the data. The application can then use standard APIs to read or write from the file.
old-location: edp\protectfiletoenterpriseidentity.htm
old-project: EDP
ms.assetid: 91993A9E-AC1D-4F3E-BCFC-9DE79F1C2C8D
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: EDP.protectfiletoenterpriseidentity, ProtectFileToEnterpriseIdentity, ProtectFileToEnterpriseIdentity function, edpwin32/ProtectFileToEnterpriseIdentity
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: edpwin32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
req.typenames: EAP_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	efswrt.dll
-	Ext-MS-Win-Security-EfsWrt-L1-1-1.dll
api_name:
-	ProtectFileToEnterpriseIdentity
product: Windows
targetos: Windows
req.lib: Efswrt.h
req.dll: Efswrt.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# ProtectFileToEnterpriseIdentity function


## -description



<div class="alert"><b>Note</b>  Windows Information Protection (WIP) policy can be applied on Windows 10, version 1607.</div>
<div> </div>Protects the data in a file to an enterprise identity, so that only users who are associated with that enterprise identity can access the data. The application can then use standard APIs to read or write from the file.


## -parameters




### -param fileOrFolderPath [in]

The path for the file or folder that you want to protect.


### -param identity [in]

The enterprise identity for which the data is protected. This identity is an email address or domain that is managed.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



