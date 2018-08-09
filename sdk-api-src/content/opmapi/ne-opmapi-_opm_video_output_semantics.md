---
UID: NE:opmapi._OPM_VIDEO_OUTPUT_SEMANTICS
title: "_OPM_VIDEO_OUTPUT_SEMANTICS"
author: windows-sdk-content
description: Specifies whether the IOPMVideoOutput interface will use Output Protection Manager (OPM) semantics or Certified Output Protection Protocol (COPP) semantics.
old-location: mf\opm_video_output_semantics.htm
old-project: medfound
ms.assetid: d52fbc40-072b-4b7a-87c2-b928563100bb
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: OPM_VIDEO_OUTPUT_SEMANTICS, OPM_VIDEO_OUTPUT_SEMANTICS enumeration [Media Foundation], OPM_VOS_COPP_SEMANTICS, OPM_VOS_OPM_SEMANTICS, _OPM_VIDEO_OUTPUT_SEMANTICS, mf.opm_video_output_semantics, opmapi/OPM_VIDEO_OUTPUT_SEMANTICS, opmapi/OPM_VOS_COPP_SEMANTICS, opmapi/OPM_VOS_OPM_SEMANTICS
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: opmapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Opmapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: OPM_VIDEO_OUTPUT_SEMANTICS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - opmapi.h
api_name:
 - OPM_VIDEO_OUTPUT_SEMANTICS
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: ADAM
---

# _OPM_VIDEO_OUTPUT_SEMANTICS enumeration


## -description


Specifies whether the <a href="https://msdn.microsoft.com/8bf43577-3535-4f62-ac81-bb7e3c329403">IOPMVideoOutput</a> interface will use Output Protection Manager (OPM) semantics or Certified Output Protection Protocol (COPP) semantics.


## -enum-fields




### -field OPM_VOS_COPP_SEMANTICS

The interface will use COPP semantics.


### -field OPM_VOS_OPM_SEMANTICS

The interface will use OPM semantics.


### -field OPM_VOS_OPM_INDIRECT_DISPLAY




## -see-also




<a href="https://msdn.microsoft.com/e72e0a5e-476d-41f0-9139-54c4c488053f">OPM Enumerations</a>



<a href="https://msdn.microsoft.com/c034ac81-43d4-482a-9dad-234d33a15046">OPMGetVideoOutputsFromHMONITOR</a>



<a href="https://msdn.microsoft.com/9b287058-9e06-4c40-84f4-506aefce5b8a">OPMGetVideoOutputsFromIDirect3DDevice9Object</a>
 

 

