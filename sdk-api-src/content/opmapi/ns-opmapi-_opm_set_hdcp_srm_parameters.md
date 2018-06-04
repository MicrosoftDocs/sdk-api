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

# _OPM_SET_HDCP_SRM_PARAMETERS structure


## -description


Contains parameters for the <a href="https://msdn.microsoft.com/ea18baba-0e03-4471-af0e-a588773c98d2">OPM_SET_HDCP_SRM</a> command.  This command updates the system renewability message (SRM) for High-Bandwidth Digital Content Protection (HDCP).
      


## -struct-fields




### -field ulSRMVersion

Contains the SRM version number in little-endian format. This number is contained in the <b>SRM Version</b> field of the SRM. For more information, see the HDCP specification.


## -see-also




<a href="https://msdn.microsoft.com/676a60ca-393e-4b5d-89d3-50cf4b771492">OPM Structures</a>



<a href="https://msdn.microsoft.com/daae615b-37c4-4044-91c6-693357e0016a">Output Protection Manager</a>
 

 

