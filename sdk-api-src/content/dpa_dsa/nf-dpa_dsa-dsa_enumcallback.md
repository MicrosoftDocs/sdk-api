---
UID: NF:dpa_dsa.DSA_EnumCallback
title: DSA_EnumCallback function (dpa_dsa.h)

description: Iterates through the dynamic structure array (DSA) and calls pfnCB on each item.
old-location: controls\DSA_EnumCallback.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\common\functions\dsa_enumcallback.htm

ms.date: 12/05/2018
ms.keywords: DSA_EnumCallback, DSA_EnumCallback function [Windows Controls], _shell_DSA_EnumCallback, _shell_DSA_EnumCallback_cpp, controls.DSA_EnumCallback, controls._shell_DSA_EnumCallback, dpa_dsa/DSA_EnumCallback
ms.topic: function
f1_keywords: 
 - "dpa_dsa/DSA_EnumCallback"
dev_langs:
 - c++
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
req.dll: Comctl32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Comctl32.dll
api_name:
 - DSA_EnumCallback
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DSA_EnumCallback function


## -description


Iterates through the  dynamic structure array (DSA) and calls <i>pfnCB</i> on each item. 


## -parameters




### -param hdsa [in]

Type: <b>HDSA</b>

A handle to an existing DSA.


### -param pfnCB [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/dpa_dsa/nc-dpa_dsa-pfndaenumcallback">PFNDAENUMCALLBACK</a>*</b>

A callback function pointer. See <a href="https://docs.microsoft.com/en-us/windows/desktop/api/dpa_dsa/nc-dpa_dsa-pfndaenumcallback">PFNDSAENUMCALLBACK</a> for the callback function prototype.


### -param pData [in]

Type: <b>void*</b>

A callback data pointer. <i>pData</i> is passed as a parameter to <i>pfnCB</i>.


## -returns



This function does not return a value.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dpa_dsa/nc-dpa_dsa-pfndaenumcallbackconst">PFNDAENUMCALLBACKCONST</a>
 

 

