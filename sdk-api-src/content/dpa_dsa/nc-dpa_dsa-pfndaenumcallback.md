---
UID: NC:dpa_dsa.PFNDAENUMCALLBACK
title: PFNDAENUMCALLBACK (dpa_dsa.h)
description: Defines the prototype for the callback function used by dynamic structure array (DSA) and dynamic pointer array (DPA) functions.
helpviewer_keywords: ["PFNDAENUMCALLBACK","PFNDAENUMCALLBACK callback","PFNDAENUMCALLBACK callback function [Windows Controls]","PFNDPAENUMCALLBACK","PFNDSAENUMCALLBACK","_shell_PFNDAENUMCALLBACK","_shell_PFNDAENUMCALLBACK_cpp","controls.PFNDAENUMCALLBACK","controls._shell_PFNDAENUMCALLBACK","dpa_dsa/PFNDAENUMCALLBACK"]
old-location: controls\PFNDAENUMCALLBACK.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\common\functions\pfndaenumcallback.htm
ms.date: 12/05/2018
ms.keywords: PFNDAENUMCALLBACK, PFNDAENUMCALLBACK callback, PFNDAENUMCALLBACK callback function [Windows Controls], PFNDPAENUMCALLBACK, PFNDSAENUMCALLBACK, _shell_PFNDAENUMCALLBACK, _shell_PFNDAENUMCALLBACK_cpp, controls.PFNDAENUMCALLBACK, controls._shell_PFNDAENUMCALLBACK, dpa_dsa/PFNDAENUMCALLBACK
req.header: dpa_dsa.h
req.include-header: 
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PFNDAENUMCALLBACK
 - dpa_dsa/PFNDAENUMCALLBACK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - dpa_dsa.h
api_name:
 - PFNDAENUMCALLBACK
---

# PFNDAENUMCALLBACK callback function


## -description

Defines the prototype for the callback function used by dynamic structure array (DSA) and dynamic pointer array (DPA) functions.

## -parameters

### -param p [in, optional]

Type: <b>void*</b>

 A pointer to the structure to be enumerated.

### -param pData [in, optional]

Type: <b>void*</b>

The value that was passed in the <i>pData</i> parameter to function <a href="/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dsa_enumcallback">DSA_EnumCallback</a>.

## -returns

Type: <b>int</b>

The return value is used to determine whether to terminate or continue the iteration. A return value of zero indicates that the iteration should stop; nonzero indicates that the iteration should continue.

## -remarks

Alternate names for this callback are <b>PFNDPAENUMCALLBACK</b> and <b>PFNDSAENUMCALLBACK</b>.
