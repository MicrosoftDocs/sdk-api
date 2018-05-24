---
UID: NF:azroles.IAzApplication.get_ApplyStoreSacl
title: IAzApplication::get_ApplyStoreSacl
author: windows-driver-content
description: Sets or retrieves a value that indicates whether policy audits should be generated when the authorization store is modified.
old-location: security\iazapplication_applystoresacl.htm
old-project: SecAuthZ
ms.assetid: 722b0693-a11f-434a-a278-780619b0077a
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: ApplyStoreSacl property [Security], ApplyStoreSacl property [Security],AzApplication object, ApplyStoreSacl property [Security],IAzApplication interface, AzApplication object [Security],ApplyStoreSacl property, IAzApplication interface [Security],ApplyStoreSacl property, IAzApplication.ApplyStoreSacl, IAzApplication.get_ApplyStoreSacl, IAzApplication::ApplyStoreSacl, IAzApplication::get_ApplyStoreSacl, IAzApplication::put_ApplyStoreSacl, azroles/IAzApplication::ApplyStoreSacl, azroles/IAzApplication::get_ApplyStoreSacl, azroles/IAzApplication::put_ApplyStoreSacl, get_ApplyStoreSacl, security.iazapplication_applystoresacl
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: azroles.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.typenames: AZ_PROP_CONSTANTS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Azroles.dll
api_name:
-	IAzApplication.ApplyStoreSacl
-	IAzApplication.get_ApplyStoreSacl
-	IAzApplication.put_ApplyStoreSacl
-	AzApplication.ApplyStoreSacl
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzApplication::get_ApplyStoreSacl


## -description


The <b>ApplyStoreSacl</b> property sets or retrieves a value that indicates whether policy audits should be generated when the authorization store is modified.

This property is read/write.


## -parameters


## -remarks



Policy audits are generated when the underlying policy store is modified. Both success and failure audits are requested.

This property controls policy auditing only for the <a href="https://msdn.microsoft.com/ea4a8a84-5003-44da-b75e-34da6bd898dd">IAzApplication</a> object and its child objects.



