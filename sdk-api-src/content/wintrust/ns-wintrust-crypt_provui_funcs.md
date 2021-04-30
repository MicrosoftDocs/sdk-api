---
UID: NS:wintrust._CRYPT_PROVUI_FUNCS
title: CRYPT_PROVUI_FUNCS (wintrust.h)
description: Provides information about the user interface (UI) functions of a provider. This structure is used by the CRYPT_PROVIDER_FUNCTIONS structure.
helpviewer_keywords: ["*PCRYPT_PROVUI_FUNCS","CRYPT_PROVUI_FUNCS","CRYPT_PROVUI_FUNCS structure [Security]","PCRYPT_PROVUI_FUNCS","PCRYPT_PROVUI_FUNCS structure pointer [Security]","security.crypt_provui_funcs","wintrust/CRYPT_PROVUI_FUNCS","wintrust/PCRYPT_PROVUI_FUNCS"]
old-location: security\crypt_provui_funcs.htm
tech.root: security
ms.assetid: 7cdc32ea-b28a-400f-ad8a-984f86bb95fd
ms.date: 12/05/2018
ms.keywords: '*PCRYPT_PROVUI_FUNCS, CRYPT_PROVUI_FUNCS, CRYPT_PROVUI_FUNCS structure [Security], PCRYPT_PROVUI_FUNCS, PCRYPT_PROVUI_FUNCS structure pointer [Security], security.crypt_provui_funcs, wintrust/CRYPT_PROVUI_FUNCS, wintrust/PCRYPT_PROVUI_FUNCS'
req.header: wintrust.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: CRYPT_PROVUI_FUNCS, *PCRYPT_PROVUI_FUNCS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPT_PROVUI_FUNCS
 - wintrust/_CRYPT_PROVUI_FUNCS
 - PCRYPT_PROVUI_FUNCS
 - wintrust/PCRYPT_PROVUI_FUNCS
 - CRYPT_PROVUI_FUNCS
 - wintrust/CRYPT_PROVUI_FUNCS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wintrust.h
api_name:
 - CRYPT_PROVUI_FUNCS
---

# CRYPT_PROVUI_FUNCS structure


## -description

<p class="CCE_Message">[The  <b>CRYPT_PROVUI_FUNCS</b> structure is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CRYPT_PROVUI_FUNCS</b> structure provides information about the user interface (UI) functions of a provider. This structure is used by the  <a href="/windows/desktop/api/wintrust/ns-wintrust-crypt_provider_functions">CRYPT_PROVIDER_FUNCTIONS</a> structure.

## -struct-fields

### -field cbStruct

The size, in bytes, of this structure.

### -field psUIData

A pointer to a <a href="/windows/desktop/api/wintrust/ns-wintrust-crypt_provui_data">CRYPT_PROVUI_DATA</a> structure.

### -field pfnOnMoreInfoClick

A pointer to the  function called when the <b>More Info</b> button is clicked.

### -field pfnOnMoreInfoClickDefault

A pointer to the  default function called when the <b>More Info</b> button is clicked.

### -field pfnOnAdvancedClick

A pointer to the  function called when the <b>Advanced</b> button is clicked.

### -field pfnOnAdvancedClickDefault

A pointer to the  default function called when the <b>Advanced</b> button is clicked.

## -remarks

The prototype for PFN_PROVUI_CALL is defined as:


```cpp
#include <windows.h>
#include <Wintrust.h>

typedef BOOL (*PFN_PROVUI_CALL)(
    IN HWND hWndSecurityDialog,
    IN struct _CRYPT_PROVIDER_DATA *pProvData
);

```

## -see-also

<a href="/windows/desktop/api/wintrust/ns-wintrust-crypt_provider_data">CRYPT_PROVIDER_DATA</a>



<a href="/windows/desktop/api/wintrust/ns-wintrust-crypt_provider_functions">CRYPT_PROVIDER_FUNCTIONS</a>