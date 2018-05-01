---
UID: NF:winddi.CLIPOBJ_bEnum
title: CLIPOBJ_bEnum function
author: windows-driver-content
description: The CLIPOBJ_bEnum function enumerates a batch of rectangles from a specified clip region; a prior call to CLIPOBJ_cEnumStart determines the order of enumeration.
old-location: display\clipobj_benum.htm
old-project: display
ms.assetid: d54e6e2a-4869-45d6-9ad1-4e9aca5f5e77
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: CLIPOBJ_bEnum, CLIPOBJ_bEnum function [Display Devices], display.clipobj_benum, gdifncs_8f383214-6bb4-4099-bdf7-c019a28ef8ac.xml, winddi/CLIPOBJ_bEnum
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows 2000 and later versions of the Windows operating systems.
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
req.typenames: SSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS, *PSSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Win32k.sys
api_name:
-	CLIPOBJ_bEnum
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# CLIPOBJ_bEnum function


## -description


The <b>CLIPOBJ_bEnum</b> function enumerates a batch of rectangles from a specified <a href="https://msdn.microsoft.com/ac439eb8-b491-4215-877d-5ee177fbdb39">clip region</a>; a prior call to <a href="https://msdn.microsoft.com/library/windows/hardware/ff539421">CLIPOBJ_cEnumStart</a> determines the order of enumeration.


## -parameters




### -param pco [in]

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff539417">CLIPOBJ</a> structure describing the clip region that is to be enumerated.


### -param cj [in]

Specifies the size, in bytes, of the buffer pointed to by <i>pv</i>.


### -param pul

TBD




#### - pv [out]

Pointer to the buffer that will receive data about the clip region in an <a href="https://msdn.microsoft.com/library/windows/hardware/ff565490">ENUMRECTS</a> structure.


## -returns



The return value is <b>TRUE</b> if the driver must call this function again for more enumeration data, or <b>FALSE</b> if the enumeration is complete. It is possible for <b>CLIPOBJ_bEnum</b> to return <b>TRUE</b> with the number of clipping rectangles equal to zero. In such cases, the driver should call <b>CLIPOBJ_bEnum</b> again without taking any action.




## -remarks



A possible loop structure for calling this function follows:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>do {
    bMore = CLIPOBJ_bEnum(pco, sizeof(buffer), &amp;buffer.c);
    for (i = 0; i &lt; buffer.c; i++) {
        .
        .
        .
    }
} while (bMore);</pre>
</td>
</tr>
</table></span></div>
The count of objects written to the buffer is written to the buffer itself.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff539417">CLIPOBJ</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff539421">CLIPOBJ_cEnumStart</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565490">ENUMRECTS</a>
 

 

