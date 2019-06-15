---
UID: NS:dxva9typ._DXVA_COPPStatusData
title: DXVA_COPPStatusData (dxva9typ.h)
author: windows-sdk-content
description: Contains the result from a Certified Output Protection Protocol (COPP) status request.
old-location: dshow\dxva_coppstatusdata.htm
tech.root: DirectShow
ms.assetid: 62172141-cda4-4713-8ae2-e1f0c5f3fba8
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DXVA_COPPStatusData, DXVA_COPPStatusData structure [DirectShow], DXVA_COPPStatusDataStructure, _DXVA_COPPStatusData, dshow.dxva_coppstatusdata, dxva9typ/DXVA_COPPStatusData
ms.topic: struct
f1_keywords: ["dxva9typ/DXVA_COPPStatusData"]
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
ms.custom: 19H1
---

# DXVA_COPPStatusData structure


## -description



Contains the result from a Certified Output Protection Protocol (COPP) status request.




## -struct-fields




### -field rApp

A 128-bit random number that was passed by the application in the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/ns-strmif-_amcoppstatusinput">AMCOPPStatusInput</a> structure.


### -field dwFlags

Status flag. See <a href="https://docs.microsoft.com/windows/desktop/api/dxva9typ/ne-dxva9typ-_copp_statusflags">COPP_StatusFlags</a>.


### -field dwData

Response to the status query. The meaning of this value depends on the status request. For more information, see <a href="https://docs.microsoft.com/windows/desktop/DirectShow/copp-query-reference">COPP Query Reference</a>.


### -field ExtendedInfoValidMask

Reserved. Must be zero.


### -field ExtendedInfoData

Reserved. Must be zero.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/using-certified-output-protection-protocol--copp">Using Certified Output Protection Protocol (COPP)</a>
 

 

