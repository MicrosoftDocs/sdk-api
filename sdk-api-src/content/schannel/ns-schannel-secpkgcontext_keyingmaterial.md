---
UID: NS:schannel._SecPkgContext_KeyingMaterial
title: SecPkgContext_KeyingMaterial (schannel.h)
description: The SecPkgContext_KeyingMaterial structure.
helpviewer_keywords: ["*PSecPkgContext_KeyingMaterial","PSecPkgContext_KeyingMaterial","PSecPkgContext_KeyingMaterial structure pointer [Security]","SecPkgContext_KeyingMaterial","SecPkgContext_KeyingMaterial structure [Security]","SecPkgContext_KeyingMaterialA","SecPkgContext_KeyingMaterialW","_SecPkgContext_KeyingMaterialInfo","schannel/PSecPkgContext_KeyingMaterial","schannel/SecPkgContext_KeyingMaterial","schannel/SecPkgContext_KeyingMaterialA","schannel/SecPkgContext_KeyingMaterialW","security.secpkgcontext_keyingmaterial"]
old-location: security\secpkgcontext_keyingmaterial.htm
tech.root: security
ms.assetid: 2F8C4316-FC03-473C-8A97-83665B3271AC
ms.date: 12/05/2018
ms.keywords: '*PSecPkgContext_KeyingMaterial, PSecPkgContext_KeyingMaterial, PSecPkgContext_KeyingMaterial structure pointer [Security], SecPkgContext_KeyingMaterial, SecPkgContext_KeyingMaterial structure [Security], SecPkgContext_KeyingMaterialA, SecPkgContext_KeyingMaterialW, _SecPkgContext_KeyingMaterialInfo, schannel/PSecPkgContext_KeyingMaterial, schannel/SecPkgContext_KeyingMaterial, schannel/SecPkgContext_KeyingMaterialA, schannel/SecPkgContext_KeyingMaterialW, security.secpkgcontext_keyingmaterial'
req.header: schannel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SecPkgContext_KeyingMaterialW (Unicode) and SecPkgContext_KeyingMaterialA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SecPkgContext_KeyingMaterial, *PSecPkgContext_KeyingMaterial
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SecPkgContext_KeyingMaterial
 - schannel/_SecPkgContext_KeyingMaterial
 - PSecPkgContext_KeyingMaterial
 - schannel/PSecPkgContext_KeyingMaterial
 - SecPkgContext_KeyingMaterial
 - schannel/SecPkgContext_KeyingMaterial
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - schannel.h
api_name:
 - SecPkgContext_KeyingMaterial
 - SecPkgContext_KeyingMaterialA
 - SecPkgContext_KeyingMaterialW
---

# SecPkgContext_KeyingMaterial structure


## -description

The <b>SecPkgContext_KeyingMaterial</b> structure  specifies the exportable keying material for the <a href="/windows/desktop/SecGloss/s-gly">security context</a>.

## -struct-fields

### -field cbKeyingMaterial

The length, in bytes, of the keying material to be exported. Must be greater than zero.

### -field pbKeyingMaterial

A pointer to the buffer containing the exported keying material. After use, deallocate the buffer by calling <a href="/windows/desktop/api/sspi/nf-sspi-freecontextbuffer">FreeContextBuffer</a>.