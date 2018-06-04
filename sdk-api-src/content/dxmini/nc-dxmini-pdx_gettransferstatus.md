---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# PDX_GETTRANSFERSTATUS callback function


## -description


The<i> DxGetTransferStatus</i> callback function is used by DirectDraw to determine which hardware bus master has completed. 


## -parameters




### -param Arg1


### -param Arg2


### -param Arg3








#### - GetTransferOutInfo

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff549521">DDGETTRANSFERSTATUSOUTINFO</a> structure that contains the transfer status information.


#### - HwDeviceExtension

Points to the miniport driver's device extension.


#### - lpInput

Reserved for system use. 


## -returns



<i>DxGetTransferStatus</i> returns DX_OK if it succeeds; otherwise, it returns one of the following error values:




## -remarks



The driver identifies the bus master by supplying the transfer ID in the DDGETTRANSFERSTATUSOUTINFO structure. The transfer ID for each bus master is originally supplied by DirectDraw in the <b>dwTransferID</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff550356">DDTRANSFERININFO</a> structure. DirectDraw passes a pointer to DDTRANSFERININFO in its call to the driver's <a href="https://msdn.microsoft.com/62e1a5f6-9777-4acf-a531-b3554eaf89a6">DxTransfer</a> function. 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff549521">DDGETTRANSFERSTATUSOUTINFO</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550356">DDTRANSFERININFO</a>



<a href="https://msdn.microsoft.com/62e1a5f6-9777-4acf-a531-b3554eaf89a6">DxTransfer</a>
 

 

