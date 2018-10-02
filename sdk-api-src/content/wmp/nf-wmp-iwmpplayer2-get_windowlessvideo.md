---
UID: NF:wmp.IWMPPlayer2.get_windowlessVideo
title: IWMPPlayer2::get_windowlessVideo
author: windows-sdk-content
description: The get_windowlessVideo method retrieves a value indicating whether the Windows Media Player control renders video in windowless mode.
old-location: wmp\iwmpplayer2_get_windowlessvideo.htm
tech.root: WMP
ms.assetid: da1cfa7c-aa79-4711-8de2-d83317e5598f
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IWMPPlayer2 interface [Windows Media Player],get_windowlessVideo method, IWMPPlayer2.get_windowlessVideo, IWMPPlayer2::get_windowlessVideo, IWMPPlayer2get_windowlessVideo, get_windowlessVideo, get_windowlessVideo method [Windows Media Player], get_windowlessVideo method [Windows Media Player],IWMPPlayer2 interface, wmp.iwmpplayer2_get_windowlessvideo, wmp/IWMPPlayer2::get_windowlessVideo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player for Windows XP or later.
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
req.dll: Wmp.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPPlayer2.get_windowlessVideo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPPlayer2::get_windowlessVideo


## -description



The <b>get_windowlessVideo</b> method retrieves a value indicating whether the Windows Media Player control renders video in windowless mode.




## -parameters




### -param pbEnabled [out]

Pointer to a <b>VARIANT_BOOL</b> indicating whether the Windows Media Player control renders video in windowless mode.


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



By default, an embedded Windows Media Player control renders video in its own window within the client area. When the <b>VARIANT_BOOL</b> retrieved by <b>get_windowlessVideo</b> equals <b>TRUE</b>, the Windows Media Player object renders video directly in the client area, so you can apply special effects or layer the video with text.

In Windows Vista, rendering video in windowless mode can degrade performance.

The <b>get_windowlessVideo</b> method is not supported for Netscape Navigator. Setting a value for this property in Navigator may yield unexpected results.

<b>Windows Media Player 10 Mobile: </b>This method always retrieves a <b>VARIANT_BOOL</b> set to <b>FALSE</b>.




## -see-also




<a href="https://msdn.microsoft.com/bf51d54d-d0aa-42ad-8180-d1f6487baac8">IWMPPlayer2 Interface</a>



<a href="https://msdn.microsoft.com/736eaf52-29bd-4223-a62d-d3d75cef1863">IWMPPlayer2::put_windowlessVideo</a>
 

 

