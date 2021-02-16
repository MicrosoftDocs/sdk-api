---
UID: NS:eaptypes._EapSimCredential
title: EapSimCredential (eaptypes.h)
description: Contains information about the SIM that is used by the EAP method for authentication.
helpviewer_keywords: ["EapSimCredential","EapSimCredential structure [EAPHost]","eaphost.eapsimcredential","eaptypes/EAPSimCredential"]
old-location: eaphost\eapsimcredential.htm
tech.root: eaphost
ms.assetid: 483BF257-BB9F-4AF6-A55C-77277AC6E21F
ms.date: 12/05/2018
ms.keywords: EapSimCredential, EapSimCredential structure [EAPHost], eaphost.eapsimcredential, eaptypes/EAPSimCredential
req.header: eaptypes.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: EapSimCredential
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _EapSimCredential
 - eaptypes/_EapSimCredential
 - EapSimCredential
 - eaptypes/EapSimCredential
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - eaptypes.h
api_name:
 - EapSimCredential
---

# EapSimCredential structure


## -description

The <b>EapSimCredential</b> structure contains information about the SIM that is used by the EAP method for authentication.

## -struct-fields

### -field iccID

A NULL-terminated Unicode string that contains the ICC-ID of the SIM.

## -see-also

<a href="/windows/desktop/api/eaptypes/ns-eaptypes-eapcredential">EapCredential</a>