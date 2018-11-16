---
UID: NC:dxmini.PDX_GETPOLARITY
title: PDX_GETPOLARITY
author: windows-sdk-content
description: The DxGetPolarity callback function returns the polarity (even or odd) of the current field being written by the video port extensions (VPE) object.
old-location: display\dxgetpolarity.htm
tech.root: display
ms.assetid: 9bce3093-8dcd-4e91-8e20-5558f2dcce75
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: DxGetPolarity, DxGetPolarity callback function [Display Devices], PDX_GETPOLARITY, PDX_GETPOLARITY callback, VideoMiniPort_DxApiFunctions_caf5417f-329e-4270-a067-8a9c9634327d.xml, display.dxgetpolarity, dxmini/DxGetPolarity
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
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
 - DxGetPolarity
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PDX_GETPOLARITY callback function


## -description


The<i> DxGetPolarity</i> callback function returns the polarity (even or odd) of the current field being written by the <a href="https://msdn.microsoft.com/a1de1905-09f3-4689-ace9-06690a1f930a">video port extensions (VPE)</a> object. 


## -parameters




### -param Arg1


### -param Arg2


### -param Arg3








#### - GetPolarityInInfo

Points to a <a href="https://msdn.microsoft.com/ee01c693-a27d-412b-ab1a-5312e41f2365">DDGETPOLARITYININFO</a> structure that contains the VPE object from which to get the polarity information.


#### - GetPolarityOutInfo

Points to a <a href="https://msdn.microsoft.com/191d6c79-6f73-44f9-8016-912e4bb70453">DDGETPOLARITYOUTINFO</a> structure that contains the polarity information for the specified VPE object.


#### - HwDeviceExtension

Points to the miniport driver's device extension.


## -returns



<i>DxGetPolarity</i> returns DX_OK if it succeeds; otherwise, it returns one of the following error values:




## -remarks



The <a href="https://msdn.microsoft.com/ee01c693-a27d-412b-ab1a-5312e41f2365">DDGETPOLARITYININFO</a> and <a href="https://msdn.microsoft.com/191d6c79-6f73-44f9-8016-912e4bb70453">DDGETPOLARITYOUTINFO</a> structures contain VPE object information.




## -see-also




<a href="https://msdn.microsoft.com/ee01c693-a27d-412b-ab1a-5312e41f2365">DDGETPOLARITYININFO</a>



<a href="https://msdn.microsoft.com/191d6c79-6f73-44f9-8016-912e4bb70453">DDGETPOLARITYOUTINFO</a>
 

 

