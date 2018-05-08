---
UID: NF:segment.IMSVidVMR9.get_SuppressEffects
title: IMSVidVMR9::get_SuppressEffects
author: windows-driver-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
old-location: mstv\imsvidvmr9_get_suppresseffects.htm
old-project: mstv
ms.assetid: 7d2d10fe-39c2-4ee1-a5c5-5624b2fbc2ef
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IMSVidVMR9 interface [Microsoft TV Technologies],get_SuppressEffects method, IMSVidVMR9.get_SuppressEffects, IMSVidVMR9::get_SuppressEffects, IMSVidVMR9get_SuppressEffects, get_SuppressEffects, get_SuppressEffects method [Microsoft TV Technologies], get_SuppressEffects method [Microsoft TV Technologies],IMSVidVMR9 interface, mstv.imsvidvmr9_get_suppresseffects, segment/IMSVidVMR9::get_SuppressEffects
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
-	IMSVidVMR9.get_SuppressEffects
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IMSVidVMR9::get_SuppressEffects


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
        



The <b>get_SuppressEffects</b> method queries whether the Video Control configures the system for optimal video playback.


## -parameters




### -param bSuppress [out]

Receives a <b>VARIANT_BOOL</b>. For more information, see <a href="https://msdn.microsoft.com/6e51ed2a-7516-4621-9ecb-0e645c6d416c">IMSVidVMR9::put_SuppressEffects</a>. The default value is VARIANT_TRUE.


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
 




## -see-also




<a href="https://msdn.microsoft.com/c96f91d4-fc6c-4422-8fc9-ea5fed10bd80">IMSVidVMR9 Interface</a>
 

 

