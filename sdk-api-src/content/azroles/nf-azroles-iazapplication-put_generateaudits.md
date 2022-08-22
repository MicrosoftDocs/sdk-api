---
UID: NF:azroles.IAzApplication.put_GenerateAudits
title: IAzApplication::put_GenerateAudits (azroles.h)
description: The GenerateAudits property of IAzApplication sets or retrieves a value that indicates whether run-time audits should be generated. (Put)
helpviewer_keywords: ["AzApplication object [Security]","GenerateAudits property","GenerateAudits property [Security]","GenerateAudits property [Security]","AzApplication object","GenerateAudits property [Security]","IAzApplication interface","IAzApplication interface [Security]","GenerateAudits property","IAzApplication.GenerateAudits","IAzApplication.put_GenerateAudits","IAzApplication::GenerateAudits","IAzApplication::get_GenerateAudits","IAzApplication::put_GenerateAudits","azroles/IAzApplication::GenerateAudits","azroles/IAzApplication::get_GenerateAudits","azroles/IAzApplication::put_GenerateAudits","put_GenerateAudits","security.iazapplication_generateaudits"]
old-location: security\iazapplication_generateaudits.htm
tech.root: security
ms.assetid: c35f612e-4a2c-46b6-913a-26b0819394f4
ms.date: 12/05/2018
ms.keywords: AzApplication object [Security],GenerateAudits property, GenerateAudits property [Security], GenerateAudits property [Security],AzApplication object, GenerateAudits property [Security],IAzApplication interface, IAzApplication interface [Security],GenerateAudits property, IAzApplication.GenerateAudits, IAzApplication.put_GenerateAudits, IAzApplication::GenerateAudits, IAzApplication::get_GenerateAudits, IAzApplication::put_GenerateAudits, azroles/IAzApplication::GenerateAudits, azroles/IAzApplication::get_GenerateAudits, azroles/IAzApplication::put_GenerateAudits, put_GenerateAudits, security.iazapplication_generateaudits
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
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
ms.custom: 19H1
f1_keywords:
 - IAzApplication::put_GenerateAudits
 - azroles/IAzApplication::put_GenerateAudits
dev_langs:
 - c++
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
---

# IAzApplication::put_GenerateAudits


## -description

The <b>GenerateAudits</b> property sets or retrieves a value that indicates whether run-time audits should be generated.

This property is read/write.

## -parameters

## -remarks

The <b>GenerateAudits</b> property controls  client context creation, client context deletion,  and access check run-time auditing. The client context can be created by a <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID), name, or token.

The <a href="/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-get_generateaudits">AzAuthorizationStore.GenerateAudits</a> property controls application initialization auditing.
