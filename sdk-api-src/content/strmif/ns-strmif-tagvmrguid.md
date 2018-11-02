---
UID: NS:strmif.tagVMRGUID
title: tagVMRGUID
author: windows-sdk-content
description: The VMRGUID structure is a member of the VMRMONITORINFO structure and is used to identify a monitor on the system (VMR-7 only).
old-location: dshow\vmrguid.htm
tech.root: DirectShow
ms.assetid: e05d986a-c044-47c9-8430-7190ad29c7ec
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: VMRGUID, VMRGUID structure [DirectShow], VMRGUIDStructure, dshow.vmrguid, strmif/VMRGUID, tagVMRGUID
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
 - VMRGUID
product: Windows
targetos: Windows
req.typenames: VMRGUID
req.redist: 
---

# tagVMRGUID structure


## -description



The <code>VMRGUID</code> structure is a member of the <a href="https://msdn.microsoft.com/87567836-c01e-4615-a8e7-9ca590b6f7c9">VMRMONITORINFO</a> structure and is used to identify a monitor on the system (VMR-7 only).




## -struct-fields




### -field pGUID

Pointer to the GUID member of the structure. <b>pGUID</b> is <b>NULL</b> if the monitor is the default DirectDraw device.


### -field GUID

Specifies the GUID for the monitor.


## -remarks



In DirectX 9.0 and later, the monitor is identified by an integer index, not by a GUID.




## -see-also




<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>
 

 

