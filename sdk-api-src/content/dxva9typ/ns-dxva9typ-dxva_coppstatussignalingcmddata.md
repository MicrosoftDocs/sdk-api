---
UID: NS:dxva9typ._DXVA_COPPStatusSignalingCmdData
title: DXVA_COPPStatusSignalingCmdData (dxva9typ.h)
description: Contains the result from a Signaling query in Certified Output Protection Protocol (COPP).helpviewer_keywords: ["DXVA_COPPStatusSignalingCmdData","DXVA_COPPStatusSignalingCmdData structure [DirectShow]","DXVA_COPPStatusSignalingCmdDataStructure","_DXVA_COPPStatusSignalingCmdData","dshow.dxva_coppstatussignalingcmddata","dxva9typ/DXVA_COPPStatusSignalingCmdData"]
old-location: dshow\dxva_coppstatussignalingcmddata.htm
tech.root: DirectShow
ms.assetid: c6bc7d84-3e4d-41f9-8309-5817029477dd
ms.date: 12/05/2018
ms.keywords: DXVA_COPPStatusSignalingCmdData, DXVA_COPPStatusSignalingCmdData structure [DirectShow], DXVA_COPPStatusSignalingCmdDataStructure, _DXVA_COPPStatusSignalingCmdData, dshow.dxva_coppstatussignalingcmddata, dxva9typ/DXVA_COPPStatusSignalingCmdData
f1_keywords:
- dxva9typ/DXVA_COPPStatusSignalingCmdData
dev_langs:
- c++
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
- DXVA_COPPStatusSignalingCmdData
targetos: Windows
req.typenames: DXVA_COPPStatusSignalingCmdData
req.redist: 
ms.custom: 19H1
---

# DXVA_COPPStatusSignalingCmdData structure


## -description



Contains the result from a Signaling query in Certified Output Protection Protocol (COPP).




## -struct-fields




### -field rApp

A 128-bit random number that was passed by the application in the <b>AMCOPPStatusInput</b> structure.


### -field dwFlags

Status flag. See <a href="https://docs.microsoft.com/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_statusflags">COPP_StatusFlags</a>.


### -field AvailableTVProtectionStandards

Bitwise <b>OR</b> of flags from the <a href="https://docs.microsoft.com/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_tvprotectionstandard">COPP_TVProtectionStandard</a> enumeration. The driver should return flags for all of the protection standards and resolutions that it supports.


### -field ActiveTVProtectionStandard

Member of the <a href="https://docs.microsoft.com/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_tvprotectionstandard">COPP_TVProtectionStandard</a> enumeration, indicating the protection standard that is currently active.


### -field TVType

Reserved.


### -field AspectRatioValidMask1

Bit mask indicating which bits of <b>AspectRatioData1</b> are valid.


### -field AspectRatioData1

Specifies the current aspect ratio value. For EN 300 294, the value is a member of the <a href="https://docs.microsoft.com/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_imageaspectratio_en300294">COPP_ImageAspectRatio_EN300294</a> enumeration.


### -field AspectRatioValidMask2

Bit mask indicating which bits of <b>AspectRatioData2</b> are valid.


### -field AspectRatioData2

Additional data element related to aspect ratio for the current protection standard. The presence and meaning of this data depends on the protection standard. This field may be used to convey End and Q0 bits for EIA-608-B, or the active format description for CEA-805-A.


### -field AspectRatioValidMask3

Bit mask indicating which bits of <b>AspectRatioData3</b> are valid.


### -field AspectRatioData3

Additional data element related to aspect ratio for the current protection standard. The presence and meaning of this data depends on the protection standard.


### -field ExtendedInfoValidMask

Array of bit masks indicating which bits in <b>ExtendedInfoData</b> are valid.


### -field ExtendedInfoData

Additional signaling elements. This array is currently not used.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/using-certified-output-protection-protocol--copp">Using Certified Output Protection Protocol (COPP)</a>
 

 

