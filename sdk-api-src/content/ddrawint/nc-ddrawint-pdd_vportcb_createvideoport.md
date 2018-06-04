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

# PDD_VPORTCB_CREATEVIDEOPORT callback function


## -description


The <b>DdVideoPortCreate</b> callback function notifies the driver that DirectDraw has created a VPE object.


## -parameters




### -param Arg1








#### - lpCreateVideoPort

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff550551">DD_CREATEVPORTDATA</a> structure that describes the created VPE object.


## -returns



<b>DdVideoPortCreate</b> returns one of the following values:




## -remarks



<b>DdVideoPortCreate</b> can be optionally implemented in DirectDraw drivers that support VPE.

<b>DdVideoPortCreate</b> can allocate memory for and initialize any private, VPE object-specific data. The driver can use the <b>dwReserved1</b> and <b>dwReserved2</b> members of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff551761">DD_VIDEOPORT_LOCAL</a> structure to store this data. This DD_VIDEOPORT_LOCAL structure is at the <b>lpVideoPort</b> member of the DD_CREATEVPORTDATA structure at <i>lpCreateVideoPort</i>. The driver cannot use or change any other members of the DD_VIDEOPORT_LOCAL structure.

If the hardware video port is implemented to use the feature connector, the driver might need to initialize the feature connector for hardware video port use.

<b>DdVideoPortCreate</b> should not turn the hardware video port on. This is accomplished in <a href="https://msdn.microsoft.com/50a55a89-bae0-4a65-96ef-3e9903f45a0c">DdVideoPortUpdate</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550551">DD_CREATEVPORTDATA</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551761">DD_VIDEOPORT_LOCAL</a>



<a href="https://msdn.microsoft.com/50a55a89-bae0-4a65-96ef-3e9903f45a0c">DdVideoPortUpdate</a>
 

 

