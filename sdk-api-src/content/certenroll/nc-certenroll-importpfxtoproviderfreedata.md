---
UID: NC:certenroll.ImportPFXToProviderFreeData
title: ImportPFXToProviderFreeData (certenroll.h)
description: Frees PFX certificate context(s).
helpviewer_keywords: ["ImportPFXToProviderFreeData","(FNIMPORTPFXTOPROVIDERFREEDATA)","(FNIMPORTPFXTOPROVIDERFREEDATA) callback function [Security]","FNIMPORTPFXTOPROVIDERFREEDATA callback","certenroll/(FNIMPORTPFXTOPROVIDERFREEDATA)","fnimportpfxtoproviderfreedata","security.fnimportpfxtoproviderfreedata","wincrypt/(FNIMPORTPFXTOPROVIDERFREEDATA)"]
old-location: security\fnimportpfxtoproviderfreedata.htm
tech.root: security
ms.assetid: F3A28405-8D6E-4930-946B-FB7D9B6518B9
ms.date: 12/05/2018
ms.keywords: ImportPFXToProviderFreeData, (FNIMPORTPFXTOPROVIDERFREEDATA), (FNIMPORTPFXTOPROVIDERFREEDATA) callback function [Security], FNIMPORTPFXTOPROVIDERFREEDATA callback, certenroll/(FNIMPORTPFXTOPROVIDERFREEDATA), fnimportpfxtoproviderfreedata, security.fnimportpfxtoproviderfreedata, wincrypt/(FNIMPORTPFXTOPROVIDERFREEDATA)
req.header: certenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ImportPFXToProviderFreeData
 - certenroll/ImportPFXToProviderFreeData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - certenroll.h
 - wincrypt.h
api_name:
 - (FNIMPORTPFXTOPROVIDERFREEDATA)
 - ImportPFXToProviderFreeData
---

# ImportPFXToProviderFreeData callback function


## -description

Frees PFX certificate context(s).

## -parameters

### -param cCert [in]

DWORD of the number of certificate contexts to free.

### -param rgpCert [in, optional]

Pointer to a certificate Context containing to free.

