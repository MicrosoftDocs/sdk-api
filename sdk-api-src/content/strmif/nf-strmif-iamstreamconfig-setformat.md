---
UID: NF:strmif.IAMStreamConfig.SetFormat
title: IAMStreamConfig::SetFormat
author: windows-sdk-content
description: The SetFormat method sets the output format on the pin.
old-location: dshow\iamstreamconfig_setformat.htm
old-project: DirectShow
ms.assetid: 8d64e5b6-e8fa-4678-92d4-3cbf92e13ddf
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: IAMStreamConfig interface [DirectShow],SetFormat method, IAMStreamConfig.SetFormat, IAMStreamConfig::SetFormat, IAMStreamConfigSetFormat, SetFormat, SetFormat method [DirectShow], SetFormat method [DirectShow],IAMStreamConfig interface, dshow.iamstreamconfig_setformat, strmif/IAMStreamConfig::SetFormat
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMStreamConfig.SetFormat
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMStreamConfig::SetFormat


## -description



The <code>SetFormat</code> method sets the output format on the pin.




## -parameters




### -param pmt [in]

Pointer to an <a href="https://msdn.microsoft.com/973697d0-2897-48b5-88ca-a88a9650eb02">AM_MEDIA_TYPE</a> structure that specifies the new format.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_INVALIDMEDIATYPE</b></dt>
</dl>
</td>
<td width="60%">
This media type is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_NOT_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The input pin is not connected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_NOT_STOPPED</b></dt>
</dl>
</td>
<td width="60%">
Cannot set the type; the filter is not stopped.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_WRONG_STATE</b></dt>
</dl>
</td>
<td width="60%">
Cannot set the type; the filter is not stopped.

</td>
</tr>
</table>
 




## -remarks



This method specifies the format for the output pin. If the pin is not connected, it will use this format for its next connection. If the pin is already connected, it will attempt to reconnect with this format. The method might fail if the other pin rejects the new type.

If this method succeeds, subsequent calls to the <a href="https://msdn.microsoft.com/288be4db-5236-40e5-bd92-d95b1bfb86fa">IPin::EnumMediaTypes</a> method will return the new type, and no others.

On most filters, this method fails if the filter is paused or running. On some compression filters, the method fails if the filter's input pin is not connected.

With some filters, you can call this method with the value <b>NULL</b> to reset the pin to its default format.

<b>Filter Developers</b>: The following remarks describe how to implement this method:

If the output pin is not connected, and the pin supports the specified media type, return S_OK. Store the media type and offer it as format number zero in the <a href="https://msdn.microsoft.com/96f102b0-e2d1-49a1-84af-aa4622cae2a9">CBasePin::GetMediaType</a> method. Do not offer other formats, and reject other formats in the <a href="https://msdn.microsoft.com/6a138679-02b7-4ccc-8881-a0d496f84f93">CBasePin::CheckMediaType</a> method.

If the pin is already connected, and the pin supports the media type, reconnect the pin with that type. If the other pin rejects the new type, return VFW_E_INVALIDMEDIATYPE and restore the original connection.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/c171763e-9108-49a0-a4b7-855c6db0a71d">IAMStreamConfig Interface</a>
 

 

