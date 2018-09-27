---
UID: NC:dxmini.PDX_GETTRANSFERSTATUS
title: PDX_GETTRANSFERSTATUS
author: windows-sdk-content
description: The DxGetTransferStatus callback function is used by DirectDraw to determine which hardware bus master has completed.
old-location: display\dxgettransferstatus.htm
tech.root: display
ms.assetid: e33ec8f0-2d1c-42cf-8b82-8f316f52e2a8
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: DxGetTransferStatus, DxGetTransferStatus callback function [Display Devices], PDX_GETTRANSFERSTATUS, PDX_GETTRANSFERSTATUS callback, VideoMiniPort_DxApiFunctions_f0260ee6-8e6c-4ab0-bad3-8d5c2ce42488.xml, display.dxgettransferstatus, dxmini/DxGetTransferStatus
ms.prod: windows
ms.technology: windows-sdk
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
 - DxGetTransferStatus
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PDX_GETTRANSFERSTATUS callback function


## -description


The<i> DxGetTransferStatus</i> callback function is used by DirectDraw to determine which hardware bus master has completed. 


## -parameters




### -param Arg1


### -param Arg2


### -param Arg3








#### - GetTransferOutInfo

Points to a <a href="https://msdn.microsoft.com/593a42be-e1e9-41e5-a006-1513c5aa5226">DDGETTRANSFERSTATUSOUTINFO</a> structure that contains the transfer status information.


#### - HwDeviceExtension

Points to the miniport driver's device extension.


#### - lpInput

Reserved for system use. 


## -returns



<i>DxGetTransferStatus</i> returns DX_OK if it succeeds; otherwise, it returns one of the following error values:




## -remarks



The driver identifies the bus master by supplying the transfer ID in the DDGETTRANSFERSTATUSOUTINFO structure. The transfer ID for each bus master is originally supplied by DirectDraw in the <b>dwTransferID</b> member of the <a href="https://msdn.microsoft.com/9e5f938d-0db6-4df6-a9c2-49840fef8c03">DDTRANSFERININFO</a> structure. DirectDraw passes a pointer to DDTRANSFERININFO in its call to the driver's <a href="https://msdn.microsoft.com/62e1a5f6-9777-4acf-a531-b3554eaf89a6">DxTransfer</a> function. 




## -see-also




<a href="https://msdn.microsoft.com/593a42be-e1e9-41e5-a006-1513c5aa5226">DDGETTRANSFERSTATUSOUTINFO</a>



<a href="https://msdn.microsoft.com/9e5f938d-0db6-4df6-a9c2-49840fef8c03">DDTRANSFERININFO</a>



<a href="https://msdn.microsoft.com/62e1a5f6-9777-4acf-a531-b3554eaf89a6">DxTransfer</a>
 

 

