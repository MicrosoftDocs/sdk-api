---
UID: NF:ocidl.IFont.ReleaseHfont
title: IFont::ReleaseHfont
author: windows-sdk-content
description: Notifies the font object that the caller that previously locked this font in the cache with IFont::AddRefHfont no longer requires the lock.
old-location: com\ifont_releasehfont.htm
tech.root: com
ms.assetid: 2c2cf2e0-d0c8-4e4f-ba5a-6b08650aee68
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: IFont interface [COM],ReleaseHfont method, IFont.ReleaseHfont, IFont::ReleaseHfont, ReleaseHfont, ReleaseHfont method [COM], ReleaseHfont method [COM],IFont interface, _ctrl_ifont_releasehfont, com.ifont_releasehfont, ocidl/IFont::ReleaseHfont
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
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
 - COM
api_location:
 - OCIdl.h
api_name:
 - IFont.ReleaseHfont
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFont::ReleaseHfont


## -description


Notifies the font object that the caller that previously locked this font in the cache with 
   <a href="https://msdn.microsoft.com/f86d52b8-e763-4948-b853-039721ae9b38">IFont::AddRefHfont</a> no longer requires the lock.


## -parameters




### -param hFont [in]

A font handle previously realized through 
      <a href="https://msdn.microsoft.com/19bfd78a-0e81-45c3-a3b8-bc893669e9f5">IFont::get_hFont</a>. This value was passed to a previous 
      call to <a href="https://msdn.microsoft.com/f86d52b8-e763-4948-b853-039721ae9b38">IFont::AddRefHfont</a> to lock the font, and the 
      caller would now like to unlock the font in the cache.


## -returns



The method supports the standard return values <b>E_UNEXPECTED</b> and 
      <b>E_INVALIDARG</b>, as well as the following values.

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
The font was unlocked successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The font was not locked in the cache. This return value is a benign notification to the caller that it 
        may have a font reference counting problem.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/3a04d2b7-b2eb-4c6c-8863-1e88321fa382">IFont</a>



<a href="https://msdn.microsoft.com/f86d52b8-e763-4948-b853-039721ae9b38">IFont::AddRefHfont</a>
 

 

