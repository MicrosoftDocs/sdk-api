---
UID: NF:segment.IMSVidVMR9.put_SuppressEffects
title: IMSVidVMR9::put_SuppressEffects method
author: windows-driver-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
old-location: mstv\imsvidvmr9_put_suppresseffects.htm
old-project: mstv
ms.assetid: 6e51ed2a-7516-4621-9ecb-0e645c6d416c
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: IMSVidVMR9, IMSVidVMR9 interface [Microsoft TV Technologies], put_SuppressEffects method, IMSVidVMR9::put_SuppressEffects, IMSVidVMR9put_SuppressEffects, mstv.imsvidvmr9_put_suppresseffects, put_SuppressEffects method [Microsoft TV Technologies], put_SuppressEffects method [Microsoft TV Technologies], IMSVidVMR9 interface, put_SuppressEffects,IMSVidVMR9.put_SuppressEffects, segment/IMSVidVMR9::put_SuppressEffects
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Segment.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: SourceSizeList
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	segment.h
api_name:
-	IMSVidVMR9.put_SuppressEffects
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IMSVidVMR9::put_SuppressEffects method


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
        



The <b>put_SuppressEffects</b> method specifies whether the Video Control configures the system for optimal video playback.


## -parameters




### -param bSuppress [in]

Specifies a Boolean value. See Remarks for more information.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



If <i>bSuppress</i> equals VARIANT_TRUE, the Video Control configures several system parameters during video playback:

<ul>
<li>Disables the screen saver timeout.</li>
<li>Disables Microsoft ClearType smoothing.</li>
<li>Disables the drop shadow effect.</li>
<li>Disables alpha-blended mouse cursors.</li>
<li>Prevents the system from turning off the display (power management).</li>
</ul>
For applications based on the Windows Graphics Device Interface (GDI), these settings improve the video playback experience. When playback stops, the Video Control restores the original system settings.

If <i>bSuppress</i> equals VARIANT_FALSE, the Video Control does not modify any of these system settings.

The default value for this property is VARIANT_TRUE. Set this property to VARIANT_FALSE if your application wants to control all of the system settings; for example, if you are providing a custom allocator-presenter (see <a href="https://msdn.microsoft.com/f654adac-12b6-47c7-99d4-0612b1532df4">IMSVidVMR9::SetAllocator</a>).




## -see-also




<a href="https://msdn.microsoft.com/c96f91d4-fc6c-4422-8fc9-ea5fed10bd80">IMSVidVMR9 Interface</a>
 

 

