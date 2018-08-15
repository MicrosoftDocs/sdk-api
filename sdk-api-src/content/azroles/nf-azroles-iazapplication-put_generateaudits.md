---
UID: NF:azroles.IAzApplication.put_GenerateAudits
title: IAzApplication::put_GenerateAudits
author: windows-sdk-content
description: The GenerateAudits property of IAzApplication sets or retrieves a value that indicates whether run-time audits should be generated.
old-location: security\iazapplication_generateaudits.htm
old-project: secauthz
ms.assetid: c35f612e-4a2c-46b6-913a-26b0819394f4
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: AzApplication object [Security],GenerateAudits property, GenerateAudits property [Security], GenerateAudits property [Security],AzApplication object, GenerateAudits property [Security],IAzApplication interface, IAzApplication interface [Security],GenerateAudits property, IAzApplication.GenerateAudits, IAzApplication.put_GenerateAudits, IAzApplication::GenerateAudits, IAzApplication::get_GenerateAudits, IAzApplication::put_GenerateAudits, azroles/IAzApplication::GenerateAudits, azroles/IAzApplication::get_GenerateAudits, azroles/IAzApplication::put_GenerateAudits, put_GenerateAudits, security.iazapplication_generateaudits
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: azroles.h
req.include-header: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
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
tech.root: 
req.typenames: AZ_PROP_CONSTANTS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.dll
api_name:
 - IAzApplication.GenerateAudits
 - IAzApplication.get_GenerateAudits
 - IAzApplication.put_GenerateAudits
 - AzApplication.GenerateAudits
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzApplication::put_GenerateAudits


## -description


The <b>GenerateAudits</b> property sets or retrieves a value that indicates whether run-time audits should be generated.

This property is read/write.


## -parameters


## -remarks



The <b>GenerateAudits</b> property controls  client context creation, client context deletion,  and access check run-time auditing. The client context can be created by a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID), name, or token.

The <a href="https://msdn.microsoft.com/e9362ae0-488d-4b6b-9a7b-c70fd85042ca">AzAuthorizationStore.GenerateAudits</a> property controls application initialization auditing.



