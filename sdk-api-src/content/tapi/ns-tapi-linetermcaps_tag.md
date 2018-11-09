---
UID: NS:tapi.linetermcaps_tag
title: linetermcaps_tag
author: windows-sdk-content
description: The LINETERMCAPS structure describes the capabilities of a line's terminal device. The LINEDEVCAPS structure can contain an array of LINETERMCAPS structures.
old-location: tapi2\linetermcaps_str.htm
tech.root: tapi
ms.assetid: 54d36126-a032-4baa-8484-6ebeb9c4adf9
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: "*LPLINETERMCAPS, LINETERMCAPS, LINETERMCAPS structure [TAPI 2.2], LPLINETERMCAPS, LPLINETERMCAPS structure pointer [TAPI 2.2], _tapi2_linetermcaps_str, linetermcaps_tag, tapi/LINETERMCAPS, tapi/LPLINETERMCAPS, tapi2.linetermcaps_str"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: tapi.h
req.include-header: 
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
 - Tapi.h
api_name:
 - LINETERMCAPS
product: Windows
targetos: Windows
req.typenames: LINETERMCAPS, *LPLINETERMCAPS
req.redist: 
---

# linetermcaps_tag structure


## -description


The 
<b>LINETERMCAPS</b> structure describes the capabilities of a line's terminal device. The 
<a href="https://msdn.microsoft.com/83e38453-bb93-4cc5-923f-d0cd2898350a">LINEDEVCAPS</a> structure can contain an array of 
<b>LINETERMCAPS</b> structures.


## -struct-fields




### -field dwTermDev

Device type of the terminal. This member uses one of the 
<a href="https://msdn.microsoft.com/3444d022-8225-4956-89a1-721b4662d557">LINETERMDEV_ Constants</a>.


### -field dwTermModes

Terminal mode(s) the terminal device is able to deal with. This member uses one of the 
<a href="https://msdn.microsoft.com/60af1687-8958-4918-be21-a13780c60974">LINETERMMODE_ Constants</a>.


### -field dwTermSharing

Sharing modes for the terminal device. This member uses one of the 
<a href="https://msdn.microsoft.com/50a52a50-4d94-4068-9ea4-bea862400036">LINETERMSHARING_ Constants</a>.


## -remarks



This structure may not be extended.




## -see-also




<a href="https://msdn.microsoft.com/83e38453-bb93-4cc5-923f-d0cd2898350a">LINEDEVCAPS</a>



<a href="https://msdn.microsoft.com/6c5a668e-9a9a-4a7a-98e9-bd8ec4b819b2">TSPI_lineGetDevCaps</a>



<a href="https://msdn.microsoft.com/c0900c5b-8791-4653-8bfc-d32e51d10c50">lineGetDevCaps</a>



<a href="https://msdn.microsoft.com/362114d9-c5b6-4b78-bb31-811eb89fe82d">lineSetTerminal</a>
 

 

