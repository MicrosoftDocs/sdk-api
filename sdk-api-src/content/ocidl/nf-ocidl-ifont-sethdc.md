---
UID: NF:ocidl.IFont.SetHdc
title: IFont::SetHdc
author: windows-sdk-content
description: Provides a device context to the font that describes the logical mapping mode.
old-location: com\ifont_sethdc.htm
tech.root: com
ms.assetid: daba0cfa-1628-415a-8161-75f7edfeeca8
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: IFont interface [COM],SetHdc method, IFont.SetHdc, IFont::SetHdc, SetHdc, SetHdc method [COM], SetHdc method [COM],IFont interface, _ctrl_ifont_sethdc, com.ifont_sethdc, ocidl/IFont::SetHdc
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
 - IFont.SetHdc
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFont::SetHdc


## -description


Provides a device context to the font that describes the logical mapping mode.


## -parameters




### -param hDC [in]

A handle to the device context in which to select the font.


## -returns



The method supports the standard return value <b>E_INVALIDARG</b>, as well as the 
      following values.

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
The font was selected successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The font selection is not supported through this font object.

</td>
</tr>
</table>
 




## -remarks



The logical mapping mode affects the font's internal computation of its point size so that when the caller 
    asks for a font handle by calling <a href="https://msdn.microsoft.com/19bfd78a-0e81-45c3-a3b8-bc893669e9f5">IFont::get_hFont</a>, the 
    font is already properly scaled to the device context.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
The caller retains ownership of this device context which must remain valid for the lifetime of 
     the font object. Thus, the device context passed should be a memory device context (from the function 
     <a href="https://msdn.microsoft.com/6ddc3705-2995-41af-af94-258aed597e17">CreateCompatibleDC</a>) and not a screen device context 
     (from <a href="https://msdn.microsoft.com/6fc443c8-da97-4196-a9ed-179a4e583849">CreateDC</a>, 
     <a href="https://msdn.microsoft.com/50b2387b-c8e4-42a8-8f0f-0bdb355adbfd">GetDC</a>, or 
     <a href="https://msdn.microsoft.com/513341d7-bed8-469c-a067-ee71dc8860f9">BeginPaint</a>) because screen device contexts are a limited system 
     resource.




## -see-also




<a href="https://msdn.microsoft.com/3a04d2b7-b2eb-4c6c-8863-1e88321fa382">IFont</a>
 

 

