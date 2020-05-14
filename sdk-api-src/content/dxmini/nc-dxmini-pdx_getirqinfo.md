---
UID: NC:dxmini.PDX_GETIRQINFO
title: PDX_GETIRQINFO (dxmini.h)
description: The DxGetIRQInfo callback function indicates that the driver manages the interrupt request.helpviewer_keywords: ["DxGetIRQInfo","DxGetIRQInfo callback function [Display Devices]","PDX_GETIRQINFO","PDX_GETIRQINFO callback","VideoMiniPort_DxApiFunctions_1e787efc-ec94-4fa0-bc13-22142c16cc8d.xml","display.dxgetirqinfo","dxmini/DxGetIRQInfo"]
old-location: display\dxgetirqinfo.htm
tech.root: display
ms.assetid: bc7463ab-1cb1-4ce5-a929-1513507a16ff
ms.date: 12/05/2018
ms.keywords: DxGetIRQInfo, DxGetIRQInfo callback function [Display Devices], PDX_GETIRQINFO, PDX_GETIRQINFO callback, VideoMiniPort_DxApiFunctions_1e787efc-ec94-4fa0-bc13-22142c16cc8d.xml, display.dxgetirqinfo, dxmini/DxGetIRQInfo
f1_keywords:
- dxmini/DxGetIRQInfo
dev_langs:
- c++
req.header: dxmini.h
req.include-header: Dxmini.h
req.target-type: Desktop
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
- UserDefined
api_location:
- dxmini.h
api_name:
- DxGetIRQInfo
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PDX_GETIRQINFO callback function


## -description


The<i> DxGetIRQInfo</i> callback function indicates that the driver manages the interrupt request.


## -parameters




### -param Arg1


### -param Arg2


### -param Arg3








#### - GetIrqInfo

Points to a <a href="https://docs.microsoft.com/windows/desktop/api/dxmini/ns-dxmini-ddgetirqinfo">DDGETIRQINFO</a> structure that contains the interrupt request information.


#### - HwDeviceExtension

Points to the miniport driver's device extension.


#### - lpInput

Reserved for system use. 


## -returns



<i>DxGetIrqInfo</i> returns DX_OK if it succeeds; otherwise, it returns one of the following error values:




## -remarks



Because the miniport driver must always manage the IRQ, this function must always set the <b>dwFlags</b> member of the DDGETIRQINFO structure at <i>GetIrqInfo</i> to IRQINFO_HANDLED. If any other flag is set, this function will fail.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dxmini/ns-dxmini-ddgetirqinfo">DDGETIRQINFO</a>
 

 

