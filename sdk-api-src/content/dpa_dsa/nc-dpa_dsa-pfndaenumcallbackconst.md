---
UID: NC:dpa_dsa.PFNDAENUMCALLBACKCONST
title: PFNDAENUMCALLBACKCONST
author: windows-sdk-content
description: Defines the prototype for the callback function used by dynamic structure array (DSA) and dynamic pointer array (DPA) functions when the items involved are pointers to constant data.
old-location: controls\PFNDAENUMCALLBACKCONST.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\common\functions\pfndaenumcallbackconst.htm
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: PFNDAENUMCALLBACKCONST, PFNDAENUMCALLBACKCONST callback, PFNDAENUMCALLBACKCONST callback function [Windows Controls], PFNDPAENUMCALLBACKCONST, PFNDSAENUMCALLBACKCONST, _shell_PFNDAENUMCALLBACKCONST, _shell_PFNDAENUMCALLBACKCONST_cpp, controls.PFNDAENUMCALLBACKCONST, controls._shell_PFNDAENUMCALLBACKCONST, dpa_dsa/PFNDAENUMCALLBACKCONST
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - dpa_dsa.h
api_name:
 - PFNDAENUMCALLBACKCONST
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PFNDAENUMCALLBACKCONST callback function


## -description


Defines the prototype for the callback function used by dynamic structure array (DSA) and dynamic pointer array (DPA) functions when the items involved are pointers to constant data.


## -parameters




### -param *p [in, optional]

Type: <b>const void*</b>

A pointer to the constant structure to be enumerated.


### -param *pData [in, optional]

Type: <b>void*</b>

A value that was passed in the <i>pData</i> parameter to function <a href="https://msdn.microsoft.com/en-us/library/Bb775657(v=VS.85).aspx">DSA_EnumCallback</a> or function <a href="https://msdn.microsoft.com/en-us/library/Bb775615(v=VS.85).aspx">DPA_EnumCallback</a>.


## -returns



Type: <b>int</b>

The return value is used to determine whether to terminate or continue the iteration. A return value of zero indicates that the iteration should stop; nonzero indicates that the iteration should continue.




## -remarks



Alternate names for this callback are <b>PFNDPAENUMCALLBACKCONST</b> and <b>PFNDSAENUMCALLBACKCONST</b>.



