---
UID: NF:certenroll.IX509PolicyServerUrl.put_Flags
title: IX509PolicyServerUrl::put_Flags (certenroll.h)
description: Specifies or retrieves a value that indicates whether the certificate enrollment policy (CEP) server policy information can be loaded from group policy, from the registry, or both. (Put)
helpviewer_keywords: ["Flags property [Security]","Flags property [Security]","IX509PolicyServerUrl interface","IX509PolicyServerUrl interface [Security]","Flags property","IX509PolicyServerUrl.Flags","IX509PolicyServerUrl.put_Flags","IX509PolicyServerUrl::Flags","IX509PolicyServerUrl::get_Flags","IX509PolicyServerUrl::put_Flags","PsfLocationGroupPolicy","PsfLocationRegistry","certenroll/IX509PolicyServerUrl::Flags","certenroll/IX509PolicyServerUrl::get_Flags","certenroll/IX509PolicyServerUrl::put_Flags","put_Flags","security.ix509policyserverurl_flags"]
old-location: security\ix509policyserverurl_flags.htm
tech.root: security
ms.assetid: 60a9dee9-6311-45b6-8fe9-f916878a64dd
ms.date: 12/05/2018
ms.keywords: Flags property [Security], Flags property [Security],IX509PolicyServerUrl interface, IX509PolicyServerUrl interface [Security],Flags property, IX509PolicyServerUrl.Flags, IX509PolicyServerUrl.put_Flags, IX509PolicyServerUrl::Flags, IX509PolicyServerUrl::get_Flags, IX509PolicyServerUrl::put_Flags, PsfLocationGroupPolicy, PsfLocationRegistry, certenroll/IX509PolicyServerUrl::Flags, certenroll/IX509PolicyServerUrl::get_Flags, certenroll/IX509PolicyServerUrl::put_Flags, put_Flags, security.ix509policyserverurl_flags
req.header: certenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Certenroll.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IX509PolicyServerUrl::put_Flags
 - certenroll/IX509PolicyServerUrl::put_Flags
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certenroll.h
api_name:
 - IX509PolicyServerUrl.Flags
 - IX509PolicyServerUrl.get_Flags
 - IX509PolicyServerUrl.put_Flags
---

# IX509PolicyServerUrl::put_Flags


## -description

The <b>Flags</b> property specifies or retrieves a value that indicates whether the certificate enrollment policy (CEP) server policy information can be loaded from group policy, from the registry, or both.

This property is read/write.

## -parameters

## -remarks

When the PsfLocationGroupPolicy and PsfLocationRegistry flags are combined, this method reads policy information from the local registry and combines it with policy information specified by group policy.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509policyserverurl">IX509PolicyServerUrl</a>
