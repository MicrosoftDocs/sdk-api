---
UID: NF:winddi.WNDOBJ_cEnumStart
title: WNDOBJ_cEnumStart function
author: windows-driver-content
description: The WNDOBJ_cEnumStart function is a callback function that sets parameters for enumeration of rectangles in the visible region of a window.
old-location: display\wndobj_cenumstart.htm
old-project: display
ms.assetid: 7d3951de-807f-4d54-a022-e2610987d965
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: WNDOBJ_cEnumStart, WNDOBJ_cEnumStart function [Display Devices], display.wndobj_cenumstart, gdifncs_25b715da-7083-4602-b503-0f3a36a2dc1f.xml, winddi/WNDOBJ_cEnumStart
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
-	WNDOBJ_cEnumStart
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# WNDOBJ_cEnumStart function


## -description


The <b>WNDOBJ_cEnumStart</b> function is a callback function that sets parameters for enumeration of rectangles in the visible region of a window.


## -parameters




### -param pwo

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff570599">WNDOBJ</a> structure created by a call to <a href="https://msdn.microsoft.com/library/windows/hardware/ff564769">EngCreateWnd</a>.


### -param iType

Specifies the type of structures to be returned by <a href="https://msdn.microsoft.com/library/windows/hardware/ff570602">WNDOBJ_bEnum</a>. This parameter can be CT_RECTANGLES, meaning that the region is to be enumerated as a list of rectangles.


### -param iDirection

Determines the order in which the rectangles are returned. This order can be essential when an overlapping <a href="https://msdn.microsoft.com/library/windows/hardware/ff556180">DrvBitBlt</a> is being performed on the same surface. If the order is not relevant to the device driver, then CD_ANY should be specified. This allows GDI to optimize its enumeration for complex regions. This parameter can be one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
CD_ANY

</td>
<td>
Any order convenient for GDI.

</td>
</tr>
<tr>
<td>
CD_LEFTDOWN

</td>
<td>
Right to left, top to bottom.

</td>
</tr>
<tr>
<td>
CD_LEFTUP

</td>
<td>
Right to left, bottom to top.

</td>
</tr>
<tr>
<td>
CD_LEFTWARDS

</td>
<td>
Left to right, vertical direction is not defined.

</td>
</tr>
<tr>
<td>
CD_RIGHTDOWN

</td>
<td>
Left to right, top to bottom.

</td>
</tr>
<tr>
<td>
CD_RIGHTUP

</td>
<td>
Left to right, bottom to top.

</td>
</tr>
<tr>
<td>
CD_UPWARDS

</td>
<td>
Bottom to top, horizontal direction is not defined.

</td>
</tr>
</table>
 


### -param cLimit

Is an indication of how many objects the driver is interested in caching. This is only used to decide when to stop counting rectangles while GDI is calculating the return value for this function. If <i>cLimit</i> is zero, counting is not done.


## -returns



The return value is a count of the number of objects that would be enumerated, provided this value is less than or equal to <i>cLimit</i>. If the count is greater than <i>cLimit</i>, the return value is 0xFFFFFFFF.




## -remarks



Enumeration can be restarted by calling this function again.

<b>WNDOBJ_cEnumStart</b> should be called only:

<ul>
<li>
In the context of the driver callback function supplied to GDI in the <a href="https://msdn.microsoft.com/library/windows/hardware/ff564769">EngCreateWnd</a> function, or the graphics DDI functions where a WNDOBJ is given. 

</li>
<li>
When the calling thread has the device lock to ensure that no client region changes occur.

</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556180">DrvBitBlt</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564769">EngCreateWnd</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564967">EngLockDriverObj</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff570599">WNDOBJ</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff570602">WNDOBJ_bEnum</a>
 

 

