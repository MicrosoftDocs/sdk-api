---
UID: NS:tapi.linetermcaps_tag
title: LINETERMCAPS (tapi.h)
author: windows-sdk-content
description: The LINETERMCAPS structure describes the capabilities of a line's terminal device. The LINEDEVCAPS structure can contain an array of LINETERMCAPS structures.
old-location: tapi2\linetermcaps_str.htm
tech.root: Tapi
ms.assetid: 54d36126-a032-4baa-8484-6ebeb9c4adf9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPLINETERMCAPS, LINETERMCAPS, LINETERMCAPS structure [TAPI 2.2], LPLINETERMCAPS, LPLINETERMCAPS structure pointer [TAPI 2.2], _tapi2_linetermcaps_str, tapi/LINETERMCAPS, tapi/LPLINETERMCAPS, tapi2.linetermcaps_str"
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
ms.custom: 19H1
---

# LINETERMCAPS structure


## -description


The 
<b>LINETERMCAPS</b> structure describes the capabilities of a line's terminal device. The 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi/ns-tapi-linedevcaps_tag">LINEDEVCAPS</a> structure can contain an array of 
<b>LINETERMCAPS</b> structures.


## -struct-fields




### -field dwTermDev

Device type of the terminal. This member uses one of the 
<a href="https://docs.microsoft.com/windows/desktop/Tapi/linetermdev--constants">LINETERMDEV_ Constants</a>.


### -field dwTermModes

Terminal mode(s) the terminal device is able to deal with. This member uses one of the 
<a href="https://docs.microsoft.com/windows/desktop/Tapi/linetermmode--constants">LINETERMMODE_ Constants</a>.


### -field dwTermSharing

Sharing modes for the terminal device. This member uses one of the 
<a href="https://docs.microsoft.com/windows/desktop/Tapi/linetermsharing--constants">LINETERMSHARING_ Constants</a>.


## -remarks



This structure may not be extended.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tapi/ns-tapi-linedevcaps_tag">LINEDEVCAPS</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tspi/nf-tspi-tspi_linegetdevcaps">TSPI_lineGetDevCaps</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi/nf-tapi-linegetdevcaps">lineGetDevCaps</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi/nf-tapi-linesetterminal">lineSetTerminal</a>
 

 

