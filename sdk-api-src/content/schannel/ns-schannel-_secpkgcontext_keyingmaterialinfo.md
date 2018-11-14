---
UID: NS:schannel._SecPkgContext_KeyingMaterialInfo
title: "_SecPkgContext_KeyingMaterialInfo"
author: windows-sdk-content
description: The SecPkgContext_KeyingMaterial structure.
old-location: security\secpkgcontext_keyingmaterial.htm
tech.root: secauthn
ms.assetid: 2F8C4316-FC03-473C-8A97-83665B3271AC
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: "*PSecPkgContext_KeyingMaterialInfo, PSecPkgContext_KeyingMaterial, PSecPkgContext_KeyingMaterial structure pointer [Security], SecPkgContext_KeyingMaterial, SecPkgContext_KeyingMaterial structure [Security], SecPkgContext_KeyingMaterialA, SecPkgContext_KeyingMaterialInfo, SecPkgContext_KeyingMaterialW, _SecPkgContext_KeyingMaterialInfo, schannel/PSecPkgContext_KeyingMaterial, schannel/SecPkgContext_KeyingMaterial, schannel/SecPkgContext_KeyingMaterialA, schannel/SecPkgContext_KeyingMaterialW, security.secpkgcontext_keyingmaterial"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
product: Windows
targetos: Windows
req.typenames: SecPkgContext_KeyingMaterialInfo, *PSecPkgContext_KeyingMaterialInfo
req.redist: 
---

# _SecPkgContext_KeyingMaterialInfo structure


## -description


The <b>SecPkgContext_KeyingMaterial</b> structure  specifies the exportable keying material for the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security context</a>.


## -struct-fields




### -field cbLabel

 


### -field pszLabel

 


### -field cbContextValue

 


### -field pbContextValue

 


### -field cbKeyingMaterial

The length, in bytes, of the keying material to be exported. Must be greater than zero.


#### - pbKeyingMaterial

A pointer to the buffer containing the exported keying material. After use, deallocate the buffer by calling <a href="https://msdn.microsoft.com/3c3d27bb-4f9a-4979-b679-1e10fa1ff221">FreeContextBuffer</a>.

