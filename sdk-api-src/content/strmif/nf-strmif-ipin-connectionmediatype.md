---
UID: NF:strmif.IPin.ConnectionMediaType
title: IPin::ConnectionMediaType
author: windows-sdk-content
description: The ConnectionMediaType method retrieves the media type for the current pin connection, if any.
old-location: dshow\ipin_connectionmediatype.htm
old-project: DirectShow
ms.assetid: f372bfa7-b0ba-43f9-ba86-cbca5d1de515
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: ConnectionMediaType, ConnectionMediaType method [DirectShow], ConnectionMediaType method [DirectShow],IPin interface, IPin interface [DirectShow],ConnectionMediaType method, IPin.ConnectionMediaType, IPin::ConnectionMediaType, IPinConnectionMediaType, dshow.ipin_connectionmediatype, strmif/IPin::ConnectionMediaType
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
 - IPin.ConnectionMediaType
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IPin::ConnectionMediaType


## -description



The <code>ConnectionMediaType</code> method retrieves the media type for the current pin connection, if any.




## -parameters




### -param pmt [out]

Pointer to an <a href="https://msdn.microsoft.com/973697d0-2897-48b5-88ca-a88a9650eb02">AM_MEDIA_TYPE</a> structure that receives the media type.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_NOT_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
Pin is not connected.

</td>
</tr>
</table>
 




## -remarks



If the pin is connected, this method copies the media type into the <a href="https://msdn.microsoft.com/973697d0-2897-48b5-88ca-a88a9650eb02">AM_MEDIA_TYPE</a> structure specified by <i>pmt</i>. The caller must free the media type's format block. You can use the Microsoft® Win32®<b>CoTaskMemFree</b> function, or the <a href="https://msdn.microsoft.com/b7ec335e-518d-4aa6-8cde-8cb92184d0b0">FreeMediaType</a> helper function.

If the pin is not connected, this method clears the media type specified by <i>pmt</i> and returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/3fcfd874-39bc-42d2-9fc9-2d8945ffa8e3">Data Flow in the Filter Graph</a>



<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/ad0ead4e-9f8e-4935-b220-306d665e50f4">IPin Interface</a>
 

 

