---
UID: NS:dxva9typ._DXVA_COPPSetSignalingCmdData
title: "_DXVA_COPPSetSignalingCmdData"
author: windows-sdk-content
description: Contains information for the Set Signal command in Certified Output Protection Protocol (COPP).
old-location: dshow\dxva_coppsetsignalingcmddata.htm
old-project: DirectShow
ms.assetid: f104b0c6-2b2f-4e6a-97e6-d73008cb80ef
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: DXVA_COPPSetSignalingCmdData, DXVA_COPPSetSignalingCmdData structure [DirectShow], DXVA_COPPSetSignalingCmdDataStructure, _DXVA_COPPSetSignalingCmdData, dshow.dxva_coppsetsignalingcmddata, dxva9typ/DXVA_COPPSetSignalingCmdData
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
req.typenames: DXVA_COPPSetSignalingCmdData
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	dxva9typ.h
api_name:
-	DXVA_COPPSetSignalingCmdData
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# _DXVA_COPPSetSignalingCmdData structure


## -description


Contains information for the Set Signal command in Certified Output Protection Protocol (COPP).

This command causes the driver to insert Wide Screen Signalling (WSS) codes or other data packets in the television signal, as required by some Analog Copy Protection (ACP) and Copy Generation Management System — Analog (CGMS-A) specifications. For example:
<ul>
<li>ETSI EN 300 294 (625i PAL): Data packets are inserted into line 23 of the signal.</li>
<li>CEA-608-B (NTSC): Data packets are inserted into line 21 of the vertical blanking interval (VBI).</li>
</ul>

## -struct-fields




### -field ActiveTVProtectionStandard


            Specifies the protection standard and format that is current active. The value is a member of the <a href="https://msdn.microsoft.com/3a724f93-8625-4594-a45b-c2e4c882b579">COPP_TVProtectionStandard</a> enumeration.
          


### -field AspectRatioChangeMask1


            Bit mask indicating which bits from <b>AspectRatioData1</b> to set in the signal.


### -field AspectRatioData1


            Specifies the aspect ratio value to be set for the current protection standard. For EN 300 294, use the <a href="https://msdn.microsoft.com/9beb172c-6255-482b-90cc-a32b2e5d3bec">COPP_ImageAspectRatio_EN300294</a> enumeration.
          


### -field AspectRatioChangeMask2


            Bit mask indicating which bits from <b>AspectRatioData2</b> to set in the signal.


### -field AspectRatioData2

An additional data element related to aspect ratio. The presence and meaning of this data depends on the protection standard. This field can be used to convey End and Q0 bits for EIA-608-B, or the active format description for CEA-805-A.


### -field AspectRatioChangeMask3


            Bit mask indicating which bits from <b>AspectRatioData3</b> to set in the signal.


### -field AspectRatioData3

An additional data element related to aspect ratio for the current protection standard. The presence and meaning of this data depends on the protection standard.


### -field ExtendedInfoChangeMask


            Array of bit masks indicating which bits in <b>ExtendedInfoData</b> to change. This array is currently not used. Set each member to zero.
          


### -field ExtendedInfoData


            Additional signaling elements to be set. This array is currently not used.
          Set each member to zero.


### -field Reserved


            Reserved. Set to zero.
          


## -see-also




<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>



<a href="https://msdn.microsoft.com/23eebe93-416b-48c8-a05f-019e38b9a660">Using Certified Output Protection Protocol (COPP)</a>
 

 

