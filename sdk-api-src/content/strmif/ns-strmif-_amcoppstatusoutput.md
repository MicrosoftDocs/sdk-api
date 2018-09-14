---
UID: NS:strmif._AMCOPPStatusOutput
title: "_AMCOPPStatusOutput"
author: windows-sdk-content
description: The AMCOPPStatusOutput structure contains the result of a Certified Output Protection Protocol (COPP) status request.
old-location: dshow\amcoppstatusoutput.htm
tech.root: DirectShow
ms.assetid: 136ce182-24c3-489d-a9c2-0121593e4b1e
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: "*LPAMCOPPStatusOutput, AMCOPPStatusOutput, AMCOPPStatusOutput structure [DirectShow], AMCOPPStatusOutputStructure, LPAMCOPPStatusOutput, LPAMCOPPStatusOutput structure pointer [DirectShow], _AMCOPPStatusOutput, dshow.amcoppstatusoutput, strmif/AMCOPPStatusOutput, strmif/LPAMCOPPStatusOutput"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: strmif.h
req.include-header: Dshow.h
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
 - strmif.h
api_name:
 - AMCOPPStatusOutput
product: Windows
targetos: Windows
req.typenames: AMCOPPStatusOutput, *LPAMCOPPStatusOutput
req.redist: 
---

# _AMCOPPStatusOutput structure


## -description



The <b>AMCOPPStatusOutput</b> structure contains the result of a Certified Output Protection Protocol (COPP) status request.




## -struct-fields




### -field macKDI

Message Authentication Code (MAC) of the status data. The driver will use AES-based one-key CBC MAC (OMAC) to calculate this value.


### -field cbSizeData

Size of the valid data in the <b>COPPStatus</b> member.


### -field COPPStatus

Buffer that contains the result of the status request.


## -see-also




<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>



<a href="https://msdn.microsoft.com/23eebe93-416b-48c8-a05f-019e38b9a660">Using Certified Output Protection Protocol (COPP)</a>
 

 

