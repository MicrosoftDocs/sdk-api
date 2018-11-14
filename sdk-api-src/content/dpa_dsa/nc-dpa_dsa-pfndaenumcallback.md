---
UID: NC:dpa_dsa.PFNDAENUMCALLBACK
title: PFNDAENUMCALLBACK
author: windows-sdk-content
description: Defines the prototype for the callback function used by dynamic structure array (DSA) and dynamic pointer array (DPA) functions.
old-location: controls\PFNDAENUMCALLBACK.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\common\functions\pfndaenumcallback.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: PFNDAENUMCALLBACK, PFNDAENUMCALLBACK callback, PFNDAENUMCALLBACK callback function [Windows Controls], PFNDPAENUMCALLBACK, PFNDSAENUMCALLBACK, _shell_PFNDAENUMCALLBACK, _shell_PFNDAENUMCALLBACK_cpp, controls.PFNDAENUMCALLBACK, controls._shell_PFNDAENUMCALLBACK, dpa_dsa/PFNDAENUMCALLBACK
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - PFNDAENUMCALLBACK
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PFNDAENUMCALLBACK callback function


## -description


Defines the prototype for the callback function used by dynamic structure array (DSA) and dynamic pointer array (DPA) functions.


## -parameters




### -param *p [in, optional]

Type: <b>void*</b>

 A pointer to the structure to be enumerated.


### -param *pData [in, optional]

Type: <b>void*</b>

The value that was passed in the <i>pData</i> parameter to function <a href="https://msdn.microsoft.com/31abb9f9-52b5-45d3-81e3-f9ccb5977597">DSA_EnumCallback</a>.


## -returns



Type: <b>int</b>

The return value is used to determine whether to terminate or continue the iteration. A return value of zero indicates that the iteration should stop; nonzero indicates that the iteration should continue.




## -remarks



Alternate names for this callback are <b>PFNDPAENUMCALLBACK</b> and <b>PFNDSAENUMCALLBACK</b>.



