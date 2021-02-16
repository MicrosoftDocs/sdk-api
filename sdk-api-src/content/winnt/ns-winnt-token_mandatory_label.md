---
UID: NS:winnt._TOKEN_MANDATORY_LABEL
title: TOKEN_MANDATORY_LABEL (winnt.h)
description: Specifies the mandatory integrity level for a token.
helpviewer_keywords: ["*PTOKEN_MANDATORY_LABEL","PTOKEN_MANDATORY_LABEL","PTOKEN_MANDATORY_LABEL structure pointer [Security]","TOKEN_MANDATORY_LABEL","TOKEN_MANDATORY_LABEL structure [Security]","_TOKEN_MANDATORY_LABEL","security.token_mandatory_label","winnt/PTOKEN_MANDATORY_LABEL","winnt/TOKEN_MANDATORY_LABEL"]
old-location: security\token_mandatory_label.htm
tech.root: security
ms.assetid: cf37eb34-ee90-43c6-97a9-c5edfcba2bc5
ms.date: 12/05/2018
ms.keywords: '*PTOKEN_MANDATORY_LABEL, PTOKEN_MANDATORY_LABEL, PTOKEN_MANDATORY_LABEL structure pointer [Security], TOKEN_MANDATORY_LABEL, TOKEN_MANDATORY_LABEL structure [Security], _TOKEN_MANDATORY_LABEL, security.token_mandatory_label, winnt/PTOKEN_MANDATORY_LABEL, winnt/TOKEN_MANDATORY_LABEL'
req.header: winnt.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: TOKEN_MANDATORY_LABEL, *PTOKEN_MANDATORY_LABEL
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TOKEN_MANDATORY_LABEL
 - winnt/_TOKEN_MANDATORY_LABEL
 - PTOKEN_MANDATORY_LABEL
 - winnt/PTOKEN_MANDATORY_LABEL
 - TOKEN_MANDATORY_LABEL
 - winnt/TOKEN_MANDATORY_LABEL
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnt.h
api_name:
 - TOKEN_MANDATORY_LABEL
---

# TOKEN_MANDATORY_LABEL structure


## -description

The <b>TOKEN_MANDATORY_LABEL</b> structure  specifies the mandatory integrity level for  a token.

## -struct-fields

### -field Label

A <a href="/windows/desktop/api/winnt/ns-winnt-sid_and_attributes">SID_AND_ATTRIBUTES</a> structure that specifies the mandatory integrity level of the token.

## -see-also

<a href="/windows/desktop/api/winnt/ne-winnt-token_information_class">TOKEN_INFORMATION_CLASS</a>