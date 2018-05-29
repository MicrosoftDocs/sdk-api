---
UID: NS:slpublic._tagSL_LICENSING_STATUS
title: "_tagSL_LICENSING_STATUS"
author: windows-sdk-content
description: Represents the licensing status.
old-location: security\sl_licensing_status.htm
old-project: SecSLApi
ms.assetid: e7c857d9-6f63-4b1c-a562-abb158914a7d
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: SL_LICENSING_STATUS, SL_LICENSING_STATUS structure [Security], _tagSL_LICENSING_STATUS, security.sl_licensing_status, slpublic/SL_LICENSING_STATUS
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: slpublic.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: SL_LICENSING_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	slpublic.h
api_name:
-	SL_LICENSING_STATUS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# _tagSL_LICENSING_STATUS structure


## -description


Represents the licensing status.


## -struct-fields




### -field SkuId

Type: <b>SLID</b>

The SKU ID.


### -field eStatus

Type: <b><a href="https://msdn.microsoft.com/8af21021-ad18-4045-8a24-0af0d39db919">SLLICENSINGSTATUS</a></b>

The licensing status.


### -field dwGraceTime

Type: <b>DWORD</b>

The grace time in minutes.


### -field dwTotalGraceDays

Type: <b>DWORD</b>

The predefined grace days in the license.


### -field hrReason

Type: <b>HRESULT</b>

The error of unlicensed status.


### -field qwValidityExpiration

Type: <b>UINT64</b>

The validity expiration day.

