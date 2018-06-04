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

# IMSVidStreamBufferSinkEvent3::LicenseChange


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
        



The <b>LicenseChange</b> method is called when the license for the content changes.


## -parameters




### -param dwProt [in]

Specifies the new license as a member of the <a href="https://msdn.microsoft.com/190b8483-91c8-4fe4-8189-637749393151">ProtType</a> enumeration.


## -returns



Return S_OK or an error code.




## -see-also




<a href="https://msdn.microsoft.com/3d76be50-0e67-4e23-8ce0-8ac9f4ad0c1c">IMSVidStreamBufferSinkEvent3 Interface</a>
 

 

