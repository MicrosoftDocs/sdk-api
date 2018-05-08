---
UID: NF:azroles.IAzAuthorizationStore.put_GenerateAudits
title: IAzAuthorizationStore::put_GenerateAudits
author: windows-driver-content
description: Sets or retrieves a value that indicates whether run-time audits should be generated.
old-location: security\azauthorizationstore_generateaudits.htm
old-project: SecAuthZ
ms.assetid: e9362ae0-488d-4b6b-9a7b-c70fd85042ca
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: AzAuthorizationStore object [Security],GenerateAudits property, GenerateAudits property [Security], GenerateAudits property [Security],AzAuthorizationStore object, GenerateAudits property [Security],IAzAuthorizationStore interface, IAzAuthorizationStore interface [Security],GenerateAudits property, IAzAuthorizationStore.GenerateAudits, IAzAuthorizationStore.put_GenerateAudits, IAzAuthorizationStore::GenerateAudits, IAzAuthorizationStore::get_GenerateAudits, IAzAuthorizationStore::put_GenerateAudits, azroles/IAzAuthorizationStore::GenerateAudits, azroles/IAzAuthorizationStore::get_GenerateAudits, azroles/IAzAuthorizationStore::put_GenerateAudits, put_GenerateAudits, security.azauthorizationstore_generateaudits
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
-	IAzAuthorizationStore.GenerateAudits
-	IAzAuthorizationStore.get_GenerateAudits
-	IAzAuthorizationStore.put_GenerateAudits
-	AzAuthorizationStore.GenerateAudits
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzAuthorizationStore::put_GenerateAudits


## -description


The <b>GenerateAudits</b> property sets or retrieves a value that indicates whether run-time audits should be generated.

This property is read/write.


## -parameters


## -remarks



The <b>GenerateAudits</b> property controls application initialization, client context creation, client context deletion,  and access check run-time auditing. The client context can be created by <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID), name, or token.



