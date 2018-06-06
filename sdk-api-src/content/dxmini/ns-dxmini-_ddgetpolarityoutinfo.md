---
UID: NS:dxmini._DDGETPOLARITYOUTINFO
title: "_DDGETPOLARITYOUTINFO"
author: windows-sdk-content
description: The DDGETPOLARITYOUTINFO structure contains the polarity information of the video port extensions (VPE) object.
old-location: display\ddgetpolarityoutinfo.htm
old-project: display
ms.assetid: 191d6c79-6f73-44f9-8016-912e4bb70453
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: "*PDDGETPOLARITYOUTINFO, DDGETPOLARITYOUTINFO, DDGETPOLARITYOUTINFO structure [Display Devices], PDDGETPOLARITYOUTINFO, PDDGETPOLARITYOUTINFO structure pointer [Display Devices], Video_Structs_eec12c7a-29ad-4c50-b85e-a78342fcbd8a.xml, _DDGETPOLARITYOUTINFO, display.ddgetpolarityoutinfo, dxmini/DDGETPOLARITYOUTINFO, dxmini/PDDGETPOLARITYOUTINFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: DDGETPOLARITYOUTINFO, *PDDGETPOLARITYOUTINFO
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
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# _DDGETPOLARITYOUTINFO structure


## -description


The DDGETPOLARITYOUTINFO structure contains the polarity information of the <a href="https://msdn.microsoft.com/a1de1905-09f3-4689-ace9-06690a1f930a">video port extensions (VPE)</a> object. 


## -struct-fields




### -field bPolarity

Indicates the polarity (even or odd) of the current field being written by the VPE object. A value of 0x00000001 indicates even, 0x00000000 indicates odd.


## -see-also




<a href="https://msdn.microsoft.com/9bce3093-8dcd-4e91-8e20-5558f2dcce75">DxGetPolarity</a>
 

 

