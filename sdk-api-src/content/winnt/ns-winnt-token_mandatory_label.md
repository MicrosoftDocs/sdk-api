---
UID: NS:winnt._TOKEN_MANDATORY_LABEL
title: TOKEN_MANDATORY_LABEL
author: windows-sdk-content
description: Specifies the mandatory integrity level for a token.
old-location: security\token_mandatory_label.htm
tech.root: secauthz
ms.assetid: cf37eb34-ee90-43c6-97a9-c5edfcba2bc5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PTOKEN_MANDATORY_LABEL, PTOKEN_MANDATORY_LABEL, PTOKEN_MANDATORY_LABEL structure pointer [Security], TOKEN_MANDATORY_LABEL, TOKEN_MANDATORY_LABEL structure [Security], _TOKEN_MANDATORY_LABEL, security.token_mandatory_label, winnt/PTOKEN_MANDATORY_LABEL, winnt/TOKEN_MANDATORY_LABEL"
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnt.h
api_name:
 - TOKEN_MANDATORY_LABEL
product: Windows
targetos: Windows
req.typenames: TOKEN_MANDATORY_LABEL, *PTOKEN_MANDATORY_LABEL
req.redist: 
---

# TOKEN_MANDATORY_LABEL structure


## -description


The <b>TOKEN_MANDATORY_LABEL</b> structure  specifies the mandatory integrity level for  a token.


## -struct-fields




### -field Label

A <a href="https://msdn.microsoft.com/d15d5a3f-6b38-4b92-b59c-ff0d27d111d9">SID_AND_ATTRIBUTES</a> structure that specifies the mandatory integrity level of the token.


## -see-also




<a href="https://msdn.microsoft.com/cb606665-1266-4e71-a145-9b04bf157cdc">TOKEN_INFORMATION_CLASS</a>
 

 

