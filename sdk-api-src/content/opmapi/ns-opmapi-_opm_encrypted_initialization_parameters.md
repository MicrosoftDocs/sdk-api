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

# _OPM_ENCRYPTED_INITIALIZATION_PARAMETERS structure


## -description


Contains initialization parameters for an <a href="https://msdn.microsoft.com/daae615b-37c4-4044-91c6-693357e0016a">Output Protection Manager</a> (OPM) session.


## -struct-fields




### -field abEncryptedInitializationParameters

Pointer to a buffer that contains encrypted initialization parameters for the session. For more information, see <a href="https://msdn.microsoft.com/7551e374-8745-405b-9879-d35a92d661ea">IOPMVideoOutput::FinishInitialization</a>.


## -remarks



The layout of this structure is identical to the <a href="https://msdn.microsoft.com/eaf220cf-111f-42fa-80db-1c69cd863258">AMCOPPSignature</a> structure used in Certified Output Protection Protocol (COPP).




## -see-also




<a href="https://msdn.microsoft.com/676a60ca-393e-4b5d-89d3-50cf4b771492">OPM Structures</a>



<a href="https://msdn.microsoft.com/daae615b-37c4-4044-91c6-693357e0016a">Output Protection Manager</a>
 

 

