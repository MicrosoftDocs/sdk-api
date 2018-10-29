---
UID: NS:ddkmapi._DDADDVPCAPTUREBUFF
title: "_DDADDVPCAPTUREBUFF"
author: windows-sdk-content
description: The DDADDVPCAPTUREBUFF structure contains the information required to add a new buffer to the internal capture queue.
old-location: display\ddaddvpcapturebuff.htm
tech.root: display
ms.assetid: 7ee3f5ce-987a-42c9-8681-5bcb9028178a
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: "*LPDDADDVPCAPTUREBUFF, DDADDVPCAPTUREBUFF, DDADDVPCAPTUREBUFF structure [Display Devices], LPDDADDVPCAPTUREBUFF, LPDDADDVPCAPTUREBUFF structure pointer [Display Devices], _DDADDVPCAPTUREBUFF, ddkmapi/DDADDVPCAPTUREBUFF, ddkmapi/LPDDADDVPCAPTUREBUFF, ddstrcts_8aed47e9-8635-4a52-aba6-7768f11f9177.xml, display.ddaddvpcapturebuff"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ddkmapi.h
req.include-header: Ddkmapi.h
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
 - ddkmapi.h
api_name:
 - DDADDVPCAPTUREBUFF
product: Windows
targetos: Windows
req.typenames: DDADDVPCAPTUREBUFF, *LPDDADDVPCAPTUREBUFF
req.redist: 
---

# _DDADDVPCAPTUREBUFF structure


## -description


The DDADDVPCAPTUREBUFF structure contains the information required to add a new buffer to the internal capture queue. 


## -struct-fields




### -field hCapture

Handle to the <a href="https://msdn.microsoft.com/a1de1905-09f3-4689-ace9-06690a1f930a">video port extensions (VPE)</a> object.


### -field dwFlags

Indicates whether the destination buffer exists in regular system memory or nonlocal display memory (AGP). This member can be one of the following values:

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td>
DDADDBUFF_INVERT

</td>
<td>
The buffer is to be inverted during capture.

</td>
</tr>
<tr>
<td>
DDADDBUFF_NONLOCALVIDMEM

</td>
<td>
The destination buffer exists in nonlocal display memory.

</td>
</tr>
<tr>
<td>
DDADDBUFF_SYSTEMMEMORY

</td>
<td>
The destination buffer exists in system memory.

</td>
</tr>
</table>
 


### -field pMDL

Points to an <a href="https://msdn.microsoft.com/a1ec4764-4e11-4fb2-b439-ad6b721eb504">MDL</a> (defined in <i>wdm.h</i>) that describes the physical pages of the destination buffer.


### -field pKEvent

Points to a KEVENT that the kernel-mode video transport sets when the destination has been filled.


### -field lpBuffInfo

Points to a <a href="https://msdn.microsoft.com/8286c433-2183-4751-be8a-30cb9cd9146d">DDCAPBUFFINFO</a> structure that the kernel-mode video transport fills in before setting the KEVENT.


## -see-also




<a href="https://msdn.microsoft.com/8286c433-2183-4751-be8a-30cb9cd9146d">DDCAPBUFFINFO</a>



<a href="https://msdn.microsoft.com/d7e6fd1c-8865-4f55-868c-856b2f875053">DD_DXAPI_ADDVPCAPTUREBUFFER</a>



<a href="https://msdn.microsoft.com/c4b38376-b54f-4fbb-b305-5951a1ea76a1">DxApi</a>
 

 

