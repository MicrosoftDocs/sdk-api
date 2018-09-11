---
UID: NF:strmif.IMpeg2Demultiplexer.CreateOutputPin
title: IMpeg2Demultiplexer::CreateOutputPin
author: windows-sdk-content
description: The CreateOutputPin method creates a new output pin on the Demux.
old-location: dshow\impeg2demultiplexer_createoutputpin.htm
tech.root: DirectShow
ms.assetid: fb863b9c-e8da-444a-b50f-37f4fe9d8164
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: CreateOutputPin, CreateOutputPin method [DirectShow], CreateOutputPin method [DirectShow],IMpeg2Demultiplexer interface, IMpeg2Demultiplexer interface [DirectShow],CreateOutputPin method, IMpeg2Demultiplexer.CreateOutputPin, IMpeg2Demultiplexer::CreateOutputPin, IMpeg2DemultiplexerCreateOutputPin, dshow.impeg2demultiplexer_createoutputpin, strmif/IMpeg2Demultiplexer::CreateOutputPin
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IMpeg2Demultiplexer.CreateOutputPin
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMpeg2Demultiplexer::CreateOutputPin


## -description



The <code>CreateOutputPin</code> method creates a new output pin on the Demux.




## -parameters




### -param pMediaType [in]

Pointer to an <a href="https://msdn.microsoft.com/973697d0-2897-48b5-88ca-a88a9650eb02">AM_MEDIA_TYPE</a> structure that specifies the media type information for the new pin.


### -param pszPinName [in]

Pointer to a wide character string that specifies a name for the new pin. The maximum length is 128 characters, including the <b>NULL</b> terminator.


### -param ppIPin [out]

Address of a variable that receives a pointer to the pin's <a href="https://msdn.microsoft.com/ad0ead4e-9f8e-4935-b220-306d665e50f4">IPin</a> interface.


## -returns



Returns an <b>HRESULT</b> value. Possible return values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
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
<dt><b>VFW_E_DUPLICATE_NAME</b></dt>
</dl>
</td>
<td width="60%">
Duplicate pin name.

</td>
</tr>
</table>
 




## -remarks



Duplicate pin names are not allowed. To configure the pin, query the returned <a href="https://msdn.microsoft.com/ad0ead4e-9f8e-4935-b220-306d665e50f4">IPin</a> interface for the <a href="https://msdn.microsoft.com/714c6b0e-3885-4026-8a83-06b37cc97d7c">IMPEG2StreamIdMap</a> interface (for program streams) or for the <a href="https://msdn.microsoft.com/45c09a02-7da8-460a-9a64-f012c2181b94">IMPEG2PIDMap</a> interface (for transport streams). Depending on which interface is queried for on the first output pin, the Demux configures itself for either transport or program stream mode. Once the Demux is configured, any calls to <b>QueryInterface</b> to retrieve the other interface will fail.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/e9242b96-0fc3-428e-b7ee-91a4f5e67305">IMpeg2Demultiplexer Interface</a>
 

 

