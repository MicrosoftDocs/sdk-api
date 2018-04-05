---
UID: NS:bdatypes.PID_MAP
title: PID_MAP
author: windows-driver-content
description: The PID_MAP structure contains identifies the contents of an MPEG-2 transport stream packet ID.
old-location: dshow\pid_map.htm
old-project: DirectShow
ms.assetid: c247ec75-483d-4587-a82f-07bbf6d277b4
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: PID_MAP, PID_MAP structure [DirectShow], PID_MAPStructure, bdatypes/PID_MAP, dshow.pid_map
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: bdatypes.h
req.include-header: Bdaiface.h
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
req.typenames: PID_MAP
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	bdatypes.h
api_name:
-	PID_MAP
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PID_MAP structure


## -description



The <code>PID_MAP</code> structure contains identifies the contents of an MPEG-2 transport stream packet ID.




## -struct-fields




### -field ulPID

Specifies the packet ID (PID)


### -field MediaSampleContent

Specifies the contents of the packet payload, as a <a href="https://msdn.microsoft.com/library/windows/hardware/ff567719">MEDIA_SAMPLE_CONTENT</a> enumeration type.


## -see-also




<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>



<a href="https://msdn.microsoft.com/d46010c4-0f16-4c97-ad10-16f7ac250390">IEnumPIDMap Interface</a>
 

 

