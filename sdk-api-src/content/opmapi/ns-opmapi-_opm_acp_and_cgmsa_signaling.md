---
UID: NS:opmapi._OPM_ACP_AND_CGMSA_SIGNALING
title: "_OPM_ACP_AND_CGMSA_SIGNALING"
author: windows-sdk-content
description: Contains the result from an OPM_GET_ACP_AND_CGMSA_SIGNALING query.
old-location: mf\opm_acp_and_cgmsa_signaling.htm
tech.root: medfound
ms.assetid: 7388bdd9-a8bc-45f4-8539-a175190fb3c3
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: OPM_ACP_AND_CGMSA_SIGNALING, OPM_ACP_AND_CGMSA_SIGNALING structure [Media Foundation], _OPM_ACP_AND_CGMSA_SIGNALING, mf.opm_acp_and_cgmsa_signaling, opmapi/OPM_ACP_AND_CGMSA_SIGNALING
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: opmapi.h
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
 - HeaderDef
api_location:
 - opmapi.h
api_name:
 - OPM_ACP_AND_CGMSA_SIGNALING
product: Windows
targetos: Windows
req.typenames: OPM_ACP_AND_CGMSA_SIGNALING
req.redist: 
---

# _OPM_ACP_AND_CGMSA_SIGNALING structure


## -description


Contains the result from an <a href="https://msdn.microsoft.com/d477fe3e-4498-450b-93b7-ce74ae9ed005">OPM_GET_ACP_AND_CGMSA_SIGNALING</a> query.


## -struct-fields




### -field rnRandomNumber

An <a href="https://msdn.microsoft.com/d3a5be4b-39d1-43da-b87e-ab4dd7815262">OPM_RANDOM_NUMBER</a> structure. This structure contains the same 128-bit random number that the application sent to the driver in the <a href="https://msdn.microsoft.com/8959c7d1-9a78-497f-8841-d3e61e9db6a3">OPM_GET_INFO_PARAMETERS</a> or <a href="https://msdn.microsoft.com/46c0c426-9730-4a0e-ab95-03b240bd55f0">OPM_COPP_COMPATIBLE_GET_INFO_PARAMETERS</a> structure.


### -field ulStatusFlags

A bitwise <b>OR</b> of <a href="https://msdn.microsoft.com/d6d85fd4-e735-4610-93e0-bb2b1782f11b">OPM Status Flags</a>.


### -field ulAvailableTVProtectionStandards

A bitwise <b>OR</b> of zero or more <a href="https://msdn.microsoft.com/8f26aa92-ed40-483e-ac78-c071619f0e12">TV Protection Standard Flags</a>. The driver will return flags for all of the protection standards and resolutions that it supports, regardless of which are now active. 


### -field ulActiveTVProtectionStandard

One value from the <a href="https://msdn.microsoft.com/8f26aa92-ed40-483e-ac78-c071619f0e12">TV Protection Standard Flags</a>, indicating the protection standard that is currently active.


### -field ulReserved

Reserved for future use. Set to zero.


### -field ulAspectRatioValidMask1

A bitmask indicating which bits of <b>ulAspectRatioData1</b> are valid.


### -field ulAspectRatioData1

The current aspect ratio. For EN 300 294, the value is a member of the <a href="https://msdn.microsoft.com/3c0fc524-b75f-4397-bd01-25be44062e8c">OPM_IMAGE_ASPECT_RATIO_EN300294</a> enumeration.


### -field ulAspectRatioValidMask2

A bitmask indicating which bits of <b>ulAspectRatioData2</b> are valid.


### -field ulAspectRatioData2

An additional data element related to aspect ratio for the current protection standard. The presence and meaning of this data depends on the protection standard. This field can be used to convey End and Q0 bits for EIA-608-B, or the active format description for CEA-805-A.


### -field ulAspectRatioValidMask3

A bitmask indicating which bits of <b>ulAspectRatioData3</b> are valid.


### -field ulAspectRatioData3

An additional data element related to aspect ratio for the current protection standard. The presence and meaning of this data depends on the protection standard.


### -field ulReserved2

Reserved for future use. Fill this array with zeros.


### -field ulReserved3

Reserved for future use.Fill this array with zeros.


## -remarks



The layout of this structure is identical to the <a href="https://msdn.microsoft.com/c6bc7d84-3e4d-41f9-8309-5817029477dd">DXVA_COPPStatusSignalingCmdData</a> structure used in Certified Output Protection Protocol (COPP).




## -see-also




<a href="https://msdn.microsoft.com/676a60ca-393e-4b5d-89d3-50cf4b771492">OPM Structures</a>



<a href="https://msdn.microsoft.com/daae615b-37c4-4044-91c6-693357e0016a">Output Protection Manager</a>
 

 

