---
UID: NS:fwpmtypes.FWPM_LAYER_STATISTICS0_
title: FWPM_LAYER_STATISTICS0_
author: windows-sdk-content
description: Stores statistics related to a layer.
old-location: fwp\fwpm_layer_statistics0.htm
tech.root: fwp
ms.assetid: cc8e0159-fe28-4718-b5fe-d38d180b3e2c
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: FWPM_LAYER_STATISTICS0, FWPM_LAYER_STATISTICS0 structure [Filtering], FWPM_LAYER_STATISTICS0_, fwp.fwpm_layer_statistics0, fwpmtypes/FWPM_LAYER_STATISTICS0
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: fwpmtypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Fwpmtypes.idl
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
 - Fwpmtypes.h
api_name:
 - FWPM_LAYER_STATISTICS0
product: Windows
targetos: Windows
req.typenames: FWPM_LAYER_STATISTICS0
req.redist: 
---

# FWPM_LAYER_STATISTICS0_ structure


## -description


The <b>FWPM_LAYER_STATISTICS0</b> structure stores statistics related to a layer.


## -struct-fields




### -field layerId

Type: <b>GUID</b>

Identifier of the layer.


### -field classifyPermitCount

Type: <b>UINT32</b>

Number of permitted connections.


### -field classifyBlockCount

Type: <b>UINT32</b>

Number of blocked connections.


### -field classifyVetoCount

Type: <b>UINT32</b>

Number of vetoed connections.


### -field numCacheEntries

Type: <b>UINT32</b>


## -remarks



<b>FWPM_LAYER_STATISTICS0</b> is a specific implementation of FWPM_LAYER_STATISTICS. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/c3ac6871-79b1-4378-8f3c-a56e85fd2a3b">FWPM_STATISTICS0</a>
 

 

