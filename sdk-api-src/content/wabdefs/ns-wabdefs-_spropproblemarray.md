---
UID: NS:wabdefs._SPropProblemArray
title: "_SPropProblemArray"
author: windows-sdk-content
description: Do not use. Contains an array of one or more SPropProblem structures.
old-location: wab\_wab_SPropProblemArray.htm
old-project: wab
ms.assetid: VS|wab|~\wab\reference\structures\spropproblemarray.htm
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*LPSPropProblemArray, SPropProblemArray, SPropProblemArray structure [Windows Address Book], _SPropProblemArray, _wab_SPropProblemArray, wab._wab_SPropProblemArray, wabdefs/SPropProblemArray"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wabdefs.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: SPropProblemArray, *LPSPropProblemArray
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wabdefs.h
api_name:
 - SPropProblemArray
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 4.0
---

# _SPropProblemArray structure


## -description


Do not use. Contains an array of one or more <a href="https://msdn.microsoft.com/a753ff2b-5d3f-4387-9124-d652f912643d">SPropProblem</a> structures.


## -struct-fields




### -field cProblem

Type: <b>ULONG</b>

Variable of type <b>ULONG</b> that specifies the count of <a href="https://msdn.microsoft.com/a753ff2b-5d3f-4387-9124-d652f912643d">SPropProblem</a> structures in the array indicated by the <b>aProblem</b> member. 


### -field aProblem

Type: <b><a href="https://msdn.microsoft.com/a753ff2b-5d3f-4387-9124-d652f912643d">SPropProblem</a>[MAPI_DIM]</b>

Array of variables of type <a href="https://msdn.microsoft.com/a753ff2b-5d3f-4387-9124-d652f912643d">SPropProblem</a> that specify information about a property error.

