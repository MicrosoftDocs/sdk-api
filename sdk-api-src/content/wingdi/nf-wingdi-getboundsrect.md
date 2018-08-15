---
UID: NF:wingdi.GetBoundsRect
title: GetBoundsRect function
author: windows-sdk-content
description: The GetBoundsRect function obtains the current accumulated bounding rectangle for a specified device context.
old-location: gdi\getboundsrect.htm
old-project: gdi
ms.assetid: 139d4550-9adc-48b3-a15c-03ae1f1ef1ab
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DCB_RESET, GetBoundsRect, GetBoundsRect function [Windows GDI], _win32_GetBoundsRect, gdi.getboundsrect, wingdi/GetBoundsRect
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wingdi.h
req.include-header: Windows.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: DISPLAYCONFIG_VIDEO_OUTPUT_TECHNOLOGY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32Full.dll
api_name:
 - GetBoundsRect
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GetBoundsRect function


## -description


The <b>GetBoundsRect</b> function obtains the current accumulated bounding rectangle for a specified device context.

The system maintains an accumulated bounding rectangle for each application. An application can retrieve and set this rectangle.


## -parameters




### -param hdc [in]

A handle to the device context whose bounding rectangle the function will return.


### -param lprect [out]

A pointer to the <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure that will receive the current bounding rectangle. The application's rectangle is returned in logical coordinates, and the bounding rectangle is returned in screen coordinates.


### -param flags [in]

Specifies how the <b>GetBoundsRect</b> function will behave. This parameter can be the following value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DCB_RESET"></a><a id="dcb_reset"></a><dl>
<dt><b>DCB_RESET</b></dt>
</dl>
</td>
<td width="60%">
Clears the bounding rectangle after returning it. If this flag is not set, the bounding rectangle will not be cleared.

</td>
</tr>
</table>
 


## -returns



The return value specifies the state of the accumulated bounding rectangle; it can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>0</td>
<td>An error occurred. The specified device context handle is invalid.</td>
</tr>
<tr>
<td>DCB_DISABLE</td>
<td>Boundary accumulation is off.</td>
</tr>
<tr>
<td>DCB_ENABLE</td>
<td>Boundary accumulation is on.</td>
</tr>
<tr>
<td>DCB_RESET</td>
<td>The bounding rectangle is empty.</td>
</tr>
<tr>
<td>DCB_SET</td>
<td>The bounding rectangle is not empty.</td>
</tr>
</table>
 




## -remarks



The DCB_SET value is a combination of the bit values DCB_ACCUMULATE and DCB_RESET. Applications that check the DCB_RESET bit to determine whether the bounding rectangle is empty must also check the DCB_ACCUMULATE bit. The bounding rectangle is empty only if the DCB_RESET bit is 1 and the DCB_ACCUMULATE bit is 0.




## -see-also




<a href="https://msdn.microsoft.com/ec18323e-c13b-4328-83bf-9e4ed4a712b8">Painting and Drawing Functions</a>



<a href="https://msdn.microsoft.com/8e6034af-4dea-4579-b476-52f6dd3d5bc7">Painting and Drawing Overview</a>



<a href="https://msdn.microsoft.com/ad361e78-42e8-4945-9395-fab983e396df">SetBoundsRect</a>
 

 

