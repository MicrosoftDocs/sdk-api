---
UID: NC:ddrawint.PDD_KERNELCB_SYNCVIDEOPORT
title: PDD_KERNELCB_SYNCVIDEOPORT
author: windows-sdk-content
description: The DdSyncVideoPortData callback function sets and modifies VPE object data before it is passed to the video miniport driver.
old-location: display\ddsyncvideoportdata.htm
tech.root: display
ms.assetid: 3726a505-c3cf-4784-886e-2f4524fb0c5b
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: DdSyncVideoPortData, DdSyncVideoPortData callback function [Display Devices], PDD_KERNELCB_SYNCVIDEOPORT, PDD_KERNELCB_SYNCVIDEOPORT callback, ddfncs_828e83a4-4723-4cf5-8eac-8b6b449765c0.xml, ddrawint/DdSyncVideoPortData, display.ddsyncvideoportdata
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: ddrawint.h
req.include-header: Winddi.h
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
 - ddrawint.h
api_name:
 - DdSyncVideoPortData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PDD_KERNELCB_SYNCVIDEOPORT callback function


## -description


The <b>DdSyncVideoPortData</b> callback function sets and modifies VPE object data before it is passed to the video miniport driver. 


## -parameters




### -param Arg1








#### - lpSyncVideoPort

Points to a <a href="https://msdn.microsoft.com/babe7d53-f278-44f7-9346-b4661b603123">DD_SYNCVIDEOPORTDATA</a> structure that contains the VPE object data. 


## -returns



<b>DdSyncVideoPortData</b> returns one of the following callback codes:




## -see-also




<a href="https://msdn.microsoft.com/babe7d53-f278-44f7-9346-b4661b603123">DD_SYNCVIDEOPORTDATA</a>
 

 

