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

# IS_ADSPEC_BODY structure


## -description


The 
<b>IS_ADSPEC_BODY</b> structure contains Integrated Services Adspec information.


## -struct-fields




### -field adspec_mh

Main header information and length, expressed as an <a href="https://msdn.microsoft.com/b67fdf53-322b-4a70-ae83-63d4365e9b57">IntServMainHdr</a> structure.


### -field adspec_genparms

General Adspec parameter fragment, followed by variable-length fragments for some or all services.


## -remarks



The variable-length fragments that follow the <b>adspec_genparams</b> member can be minimal length fragments.




## -see-also




<a href="https://msdn.microsoft.com/b67fdf53-322b-4a70-ae83-63d4365e9b57">IntServMainHdr</a>
 

 

