---
UID: NF:setupapi.SetupDiDrawMiniIcon
title: SetupDiDrawMiniIcon function
author: windows-driver-content
description: The SetupDiDrawMiniIcon function draws the specified mini-icon at the location requested.
old-location: devinst\setupdidrawminiicon.htm
old-project: devinst
ms.assetid: 99670376-a338-4001-bede-a4fea57b73a7
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: SetupDiDrawMiniIcon, SetupDiDrawMiniIcon function [Device and Driver Installation], devinst.setupdidrawminiicon, di-rtns_b85627e0-4b6a-4198-b4b9-8a1afaa09a9a.xml, setupapi/SetupDiDrawMiniIcon
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: setupapi.h
req.include-header: Setupapi.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Microsoft Windows 2000 and later versions of Windows.
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
req.typenames: TSSD_ConnectionPoint, *PTSSD_ConnectionPoint
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Setupapi.dll
api_name:
-	SetupDiDrawMiniIcon
product: Windows
targetos: Windows
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# SetupDiDrawMiniIcon function


## -description


The <b>SetupDiDrawMiniIcon</b> function draws the specified mini-icon at the location requested.


## -parameters




### -param hdc [in]

The handle to the device context in which the mini-icon will be drawn.


### -param rc [in]

The rectangle in the specified device context handle to draw the mini-icon in.


### -param MiniIconIndex [in]

The index of the mini-icon, as retrieved from <a href="https://msdn.microsoft.com/library/windows/hardware/ff552053">SetupDiLoadClassIcon</a> or <a href="https://msdn.microsoft.com/library/windows/hardware/ff551047">SetupDiGetClassBitmapIndex</a>. The following predefined indexes for devices can be used:

<table>
<tr>
<th>        Class</th>
<th>Index</th>
</tr>
<tr>
<td>
        Computer/System

</td>
<td>
0

</td>
</tr>
<tr>
<td>
        Display/Monitor

</td>
<td>
2

</td>
</tr>
<tr>
<td>
        Network Adapter

</td>
<td>
3

</td>
</tr>
<tr>
<td>
        Mouse

</td>
<td>
5

</td>
</tr>
<tr>
<td>
        Keyboard

</td>
<td>
6

</td>
</tr>
<tr>
<td>
        Sound

</td>
<td>
8

</td>
</tr>
<tr>
<td>
        FDC/HDC

</td>
<td>
9

</td>
</tr>
<tr>
<td>
        Ports

</td>
<td>
10

</td>
</tr>
<tr>
<td>
        Printer

</td>
<td>
14

</td>
</tr>
<tr>
<td>
        Network Transport

</td>
<td>
15

</td>
</tr>
<tr>
<td>
        Network Client

</td>
<td>
16

</td>
</tr>
<tr>
<td>
        Network Service

</td>
<td>
17

</td>
</tr>
<tr>
<td>
        Unknown

</td>
<td>
18

</td>
</tr>
</table>
 


### -param Flags [in]

These flags control the drawing operation. The LOWORD contains the actual flags defined as follows:





#### DMI_MASK

Draw the mini-icon's mask into HDC.



#### DMI_BKCOLOR

Use the system color index specified in the HIWORD of <i>Flags</i> as the background color. If this flag is not set, COLOR_WINDOW is used.



#### DMI_USERECT

If set, <b>SetupDiDrawMiniIcon</b> uses the supplied rectangle and stretches the icon to fit.


## -returns



This function returns the offset from the left side of <i>rc</i> where the string should start. If the draw operation fails, the function returns zero.




## -remarks



By default, the icon is centered vertically and forced against the left side of the specified rectangle.

<b>SetupDiDrawMiniIcon</b> draws the 16-bit version of the icon that is specified by the <i>MiniIconIndex </i>parameter. Instead of <b>SetupDiDrawMiniIcon</b>, you should use <a href="https://msdn.microsoft.com/library/windows/hardware/ff552053">SetupDiLoadClassIcon</a> together with <b>DrawIcon</b> or <b>DrawIconEx</b> to draw the 32-bit version of the icon. The following is an example of how to use <b>DrawIconEx</b> to display an icon:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>HICON hIcon;

if (SetupDiLoadClassIcon(&amp;GUID_DEVCLASS_USB, &amp;hIcon, NULL)) {
    DrawIconEx(hDC, 0, 0, hIcon, GetSystemMetrics(SM_CXSMICON),GetSystemMetrics(SM_CYSMICON), 0, NULL, DI_NORMAL); 
DestroyIcon(hIcon);
}</pre>
</td>
</tr>
</table></span></div>
For more information about <a href="http://go.microsoft.com/fwlink/p/?linkid=181019">DrawIcon</a> or <a href="http://go.microsoft.com/fwlink/p/?linkid=181020">DrawIconEx</a>, refer to the Microsoft Windows Software Development Kit (SDK) for Windows 7 and .NET Framework 4.0 documentation.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff551047">SetupDiGetClassBitmapIndex</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552053">SetupDiLoadClassIcon</a>
 

 

