---
UID: NS:dxmini._DDGETTRANSFERSTATUSOUTINFO
title: "_DDGETTRANSFERSTATUSOUTINFO"
author: windows-driver-content
description: The DDGETTRANSFERSTATUSOUTINFO structure contains the transfer status information.
old-location: display\ddgettransferstatusoutinfo.htm
old-project: display
ms.assetid: 593a42be-e1e9-41e5-a006-1513c5aa5226
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: "*PDDGETTRANSFEROUTINFO, DDGETTRANSFERSTATUSOUTINFO, DDGETTRANSFERSTATUSOUTINFO structure [Display Devices], PDDGETTRANSFEROUTINFO, PDDGETTRANSFEROUTINFO structure pointer [Display Devices], Video_Structs_6471d175-cf52-4da4-b0c8-a4d7b96a0bea.xml, _DDGETTRANSFERSTATUSOUTINFO, display.ddgettransferstatusoutinfo, dxmini/DDGETTRANSFERSTATUSOUTINFO, dxmini/PDDGETTRANSFEROUTINFO"
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: DDGETTRANSFERSTATUSOUTINFO, *PDDGETTRANSFEROUTINFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	dxmini.h
api_name:
-	DDGETTRANSFERSTATUSOUTINFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# _DDGETTRANSFERSTATUSOUTINFO structure


## -description


The DDGETTRANSFERSTATUSOUTINFO structure contains the transfer status information. 


## -struct-fields




### -field dwTransferID

Contains the transfer ID of the bus master transfer that completed. The transfer ID was originally supplied to the driver in the <b>dwTransferID</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff550356">DDTRANSFERININFO</a> structure. The driver receives a pointer to DDTRANSFERININFO in a call to its <a href="https://msdn.microsoft.com/62e1a5f6-9777-4acf-a531-b3554eaf89a6">DxTransfer</a> function. 


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550356">DDTRANSFERININFO</a>



<a href="https://msdn.microsoft.com/e33ec8f0-2d1c-42cf-8b82-8f316f52e2a8">DxGetTransferStatus</a>



<a href="https://msdn.microsoft.com/62e1a5f6-9777-4acf-a531-b3554eaf89a6">DxTransfer</a>
 

 

