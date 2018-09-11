---
UID: NS:dxva9typ._DXVA_COPPStatusData
title: "_DXVA_COPPStatusData"
author: windows-sdk-content
description: Contains the result from a Certified Output Protection Protocol (COPP) status request.
old-location: dshow\dxva_coppstatusdata.htm
tech.root: DirectShow
ms.assetid: 62172141-cda4-4713-8ae2-e1f0c5f3fba8
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: DXVA_COPPStatusData, DXVA_COPPStatusData structure [DirectShow], DXVA_COPPStatusDataStructure, _DXVA_COPPStatusData, dshow.dxva_coppstatusdata, dxva9typ/DXVA_COPPStatusData
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: dxva9typ.h
req.include-header: Dxva.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - HeaderDef
api_location:
 - dxva9typ.h
api_name:
 - DXVA_COPPStatusData
product: Windows
targetos: Windows
req.typenames: DXVA_COPPStatusData
req.redist: 
---

# _DXVA_COPPStatusData structure


## -description



Contains the result from a Certified Output Protection Protocol (COPP) status request.




## -struct-fields




### -field rApp

A 128-bit random number that was passed by the application in the <a href="https://msdn.microsoft.com/988e6d54-f241-4cfc-8793-fc42de92ac52">AMCOPPStatusInput</a> structure.


### -field dwFlags

Status flag. See <a href="https://msdn.microsoft.com/9109bb2c-1422-4629-b2df-ac877d3cd86e">COPP_StatusFlags</a>.


### -field dwData

Response to the status query. The meaning of this value depends on the status request. For more information, see <a href="https://msdn.microsoft.com/11eb1443-857d-4516-a5cb-c3cc02a5eba4">COPP Query Reference</a>.


### -field ExtendedInfoValidMask

Reserved. Must be zero.


### -field ExtendedInfoData

Reserved. Must be zero.


## -see-also




<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>



<a href="https://msdn.microsoft.com/23eebe93-416b-48c8-a05f-019e38b9a660">Using Certified Output Protection Protocol (COPP)</a>
 

 

