---
UID: NS:accctrl._INHERITED_FROMW
title: INHERITED_FROMW (accctrl.h)
description: Provides information about an object's inherited access control entry (ACE).
helpviewer_keywords: ["*PINHERITED_FROMW","INHERITED_FROM","INHERITED_FROM structure [Security]","INHERITED_FROMA","INHERITED_FROMW","PINHERITED_FROM","PINHERITED_FROM structure pointer [Security]","_INHERITED_FROMA","_INHERITED_FROMW","accctrl/INHERITED_FROM","accctrl/INHERITED_FROMA","accctrl/INHERITED_FROMW","accctrl/PINHERITED_FROM","security.inherited_from"]
old-location: security\inherited_from.htm
tech.root: SecAuthZ
ms.assetid: 6839f67a-6c72-406d-b55e-bc366aaad107
ms.date: 12/05/2018
ms.keywords: '*PINHERITED_FROMW, INHERITED_FROM, INHERITED_FROM structure [Security], INHERITED_FROMA, INHERITED_FROMW, PINHERITED_FROM, PINHERITED_FROM structure pointer [Security], _INHERITED_FROMA, _INHERITED_FROMW, accctrl/INHERITED_FROM, accctrl/INHERITED_FROMA, accctrl/INHERITED_FROMW, accctrl/PINHERITED_FROM, security.inherited_from'
f1_keywords:
- accctrl/INHERITED_FROM
dev_langs:
- c++
req.header: accctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: INHERITED_FROMW (Unicode) and INHERITED_FROMA (ANSI)
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
- AccCtrl.h
api_name:
- INHERITED_FROM
- INHERITED_FROMA
- INHERITED_FROMW
targetos: Windows
req.typenames: INHERITED_FROMW, *PINHERITED_FROMW
req.redist: 
ms.custom: 19H1
---

# INHERITED_FROMW structure


## -description


The <b>INHERITED_FROM</b> structure provides information about an object's inherited <a href="https://docs.microsoft.com/windows/desktop/SecGloss/a-gly">access control entry</a> (ACE).


## -struct-fields




### -field GenerationGap

Number of levels, or generations, between the object and the ancestor. Set this to zero for an explicit ACE. If the ancestor cannot be determined for the inherited ACE, set this member to –1.


### -field AncestorName

Name of the ancestor from which the ACE was inherited. For an explicit ACE, set this to <b>NULL</b>.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/aclapi/nf-aclapi-freeinheritedfromarray">FreeInheritedFromArray</a>



<a href="https://docs.microsoft.com/windows/desktop/api/aclapi/nf-aclapi-getinheritancesourcea">GetInheritanceSource</a>
 

 

