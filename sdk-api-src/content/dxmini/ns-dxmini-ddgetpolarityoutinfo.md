---
UID: NS:dxmini._DDGETPOLARITYOUTINFO
title: DDGETPOLARITYOUTINFO (dxmini.h)
author: windows-sdk-content
description: The DDGETPOLARITYOUTINFO structure contains the polarity information of the video port extensions (VPE) object.
old-location: display\ddgetpolarityoutinfo.htm
tech.root: display
ms.assetid: 191d6c79-6f73-44f9-8016-912e4bb70453
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PDDGETPOLARITYOUTINFO, DDGETPOLARITYOUTINFO, DDGETPOLARITYOUTINFO structure [Display Devices], PDDGETPOLARITYOUTINFO, PDDGETPOLARITYOUTINFO structure pointer [Display Devices], Video_Structs_eec12c7a-29ad-4c50-b85e-a78342fcbd8a.xml, display.ddgetpolarityoutinfo, dxmini/DDGETPOLARITYOUTINFO, dxmini/PDDGETPOLARITYOUTINFO"
ms.topic: struct
f1_keywords: ["dxmini/DDGETPOLARITYOUTINFO"]
req.header: dxmini.h
req.include-header: Dxmini.h
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
 - dxmini.h
api_name:
 - DDGETPOLARITYOUTINFO
product: Windows
targetos: Windows
req.typenames: DDGETPOLARITYOUTINFO, *PDDGETPOLARITYOUTINFO
req.redist: 
ms.custom: 19H1
---

# DDGETPOLARITYOUTINFO structure


## -description


The DDGETPOLARITYOUTINFO structure contains the polarity information of the <a href="https://docs.microsoft.com/windows-hardware/drivers/">video port extensions (VPE)</a> object. 


## -struct-fields




### -field bPolarity

Indicates the polarity (even or odd) of the current field being written by the VPE object. A value of 0x00000001 indicates even, 0x00000000 indicates odd.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dxmini/nc-dxmini-pdx_getpolarity">DxGetPolarity</a>
 

 

