---
UID: NF:wmsdkidl.IWMReaderAdvanced2.OpenStream
title: IWMReaderAdvanced2::OpenStream (wmsdkidl.h)
author: windows-sdk-content
description: The OpenStream method opens a Windows Media stream for reading.
old-location: wmformat\iwmreaderadvanced2_openstream.htm
tech.root: wmformat
ms.assetid: 20822e1d-b367-4b03-9d8a-985427f0062d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMReaderAdvanced2 interface [windows Media Format],OpenStream method, IWMReaderAdvanced2.OpenStream, IWMReaderAdvanced2::OpenStream, IWMReaderAdvanced2OpenStream, OpenStream, OpenStream method [windows Media Format], OpenStream method [windows Media Format],IWMReaderAdvanced2 interface, wmformat.iwmreaderadvanced2_openstream, wmsdkidl/IWMReaderAdvanced2::OpenStream
ms.topic: method
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 7 SDK, or later versions of the SDK
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
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmvcore.lib
 - Wmvcore.dll
 - WMStubDRM.lib
 - WMStubDRM.dll
api_name:
 - IWMReaderAdvanced2.OpenStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMReaderAdvanced2::OpenStream


## -description



The <b>OpenStream</b> method opens a Windows Media stream for reading.




## -parameters




### -param pStream [in]

Pointer to an <b>IStream</b> interface (see the Remarks section below).


### -param pCallback [in]

Pointer to an <a href="https://msdn.microsoft.com/en-us/library/Dd743493(v=VS.85).aspx">IWMReaderCallback</a> interface.


### -param pvContext [in]

Generic pointer, for use by the application. This is passed to the application in calls to <b>IWMReaderCallback::OnStatus</b>.


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
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pCallback</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough available memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The method failed for an unspecified reason.

</td>
</tr>
</table>
 




## -remarks



This method is identical to <a href="https://msdn.microsoft.com/en-us/library/Dd743597(v=VS.85).aspx">IWMReader::Open</a>, except that it takes an <b>IStream</b> interface pointer instead of a URL. An <b>IStream</b> is a standard COM interface for providing data. This allows the application to provide its own data, rather than just getting data from a file or a network. For example, if you have an <b>IStream</b> interface pointer that represents the contents of a supported media file (Windows Media Audio, Windows Media Video, MP3, for example) and, for performance reasons, you do not want to write a temporary file , this is a way you can use the SDK to parse and decompress your content.

This method sends a WMT_OPENED status notification to the application's <b>IWMReaderCallback::OnStatus</b> function. (<a href="https://msdn.microsoft.com/en-us/library/Dd798545(v=VS.85).aspx">OnStatus</a> is inherited by <b>IWMReaderCallback</b> from <a href="https://msdn.microsoft.com/en-us/library/Dd798544(v=VS.85).aspx">IWMStatusCallback</a>.)




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd757430(v=VS.85).aspx">IWMReaderAdvanced2 Interface</a>
 

 

