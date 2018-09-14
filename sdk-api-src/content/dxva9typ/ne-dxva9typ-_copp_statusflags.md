---
UID: NE:dxva9typ._COPP_StatusFlags
title: "_COPP_StatusFlags"
author: windows-sdk-content
description: Specifies the status of a Certified Output Protection Protocol (COPP) session.
old-location: dshow\copp_statusflags.htm
tech.root: DirectShow
ms.assetid: 9109bb2c-1422-4629-b2df-ac877d3cd86e
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: COPP_LinkLost, COPP_RenegotiationRequired, COPP_StatusFlags, COPP_StatusFlags , COPP_StatusFlags enumeration [DirectShow], COPP_StatusFlagsEnumeration, COPP_StatusFlagsReserved, COPP_StatusNormal, _COPP_StatusFlags, dshow.copp_statusflags, dxva9typ/COPP_LinkLost, dxva9typ/COPP_RenegotiationRequired, dxva9typ/COPP_StatusFlags, dxva9typ/COPP_StatusFlagsReserved, dxva9typ/COPP_StatusNormal
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: dxva9typ.h
req.include-header: Dxva.h
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
 - dxva9typ.h
api_name:
 - COPP_StatusFlags
product: Windows
targetos: Windows
req.typenames: COPP_StatusFlags
req.redist: 
---

# _COPP_StatusFlags enumeration


## -description



Specifies the status of a Certified Output Protection Protocol (COPP) session.




## -enum-fields




### -field COPP_StatusNormal

Normal status.
          


### -field COPP_LinkLost

The integrity of the connection has been compromised. Examples of events that cause the driver to set this flag include:

<ul>
<li>The driver can no longer enforce the current protection level.</li>
<li>The driver detected an internal integrity error.</li>
<li>The connector between the computer and the display device was unplugged.</li>
</ul>

### -field COPP_RenegotiationRequired

The connection configuration has changed. For example, the user has changed the desktop display mode.
          


### -field COPP_StatusFlagsReserved

Reserved. Must be zero.
          


## -remarks



If COPP_LinkLost is returned, the application should release the current instance of the VMR, create a new instance of the VMR, and establish a new COPP session (including key exchange and certificate validation).




## -see-also




<a href="https://msdn.microsoft.com/74467006-b077-49c0-8573-f939ac3d3444">DirectShow Enumerated Types</a>



<a href="https://msdn.microsoft.com/23eebe93-416b-48c8-a05f-019e38b9a660">Using Certified Output Protection Protocol (COPP)</a>
 

 

