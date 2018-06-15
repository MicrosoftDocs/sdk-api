---
UID: NF:wmsdkidl.IWMReaderAdvanced.SetReceiveStreamSamples
title: IWMReaderAdvanced::SetReceiveStreamSamples
author: windows-sdk-content
description: The SetReceiveStreamSamples method specifies whether stream samples are delivered to the IWMReaderCallbackAdvanced::OnStreamSample callback.
old-location: wmformat\iwmreaderadvanced_setreceivestreamsamples.htm
old-project: wmformat
ms.assetid: 3fb39726-7f43-41ec-9ead-38456b5cd964
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: IWMReaderAdvanced interface [windows Media Format],SetReceiveStreamSamples method, IWMReaderAdvanced.SetReceiveStreamSamples, IWMReaderAdvanced::SetReceiveStreamSamples, IWMReaderAdvancedSetReceiveStreamSamples, SetReceiveStreamSamples, SetReceiveStreamSamples method [windows Media Format], SetReceiveStreamSamples method [windows Media Format],IWMReaderAdvanced interface, wmformat.iwmreaderadvanced_setreceivestreamsamples, wmsdkidl/IWMReaderAdvanced::SetReceiveStreamSamples
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WM_AETYPE
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
 - IWMReaderAdvanced.SetReceiveStreamSamples
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMReaderAdvanced::SetReceiveStreamSamples


## -description



The <b>SetReceiveStreamSamples</b> method specifies whether stream samples are delivered to the <a href="https://msdn.microsoft.com/6bfdd903-a3a4-4ef4-b88a-4d24c9c0f4b8">IWMReaderCallbackAdvanced::OnStreamSample</a> callback.




## -parameters




### -param wStreamNum [in]

<b>WORD</b> containing the stream number. Stream numbers are in the range of 1 through 63.


### -param fReceiveStreamSamples [in]

Boolean value that is True if stream samples are delivered.


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
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The method failed for an unspecified reason.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
No callback interface has been specified.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_PROTECTED_CONTENT</b></dt>
</dl>
</td>
<td width="60%">
Attempted read on a file protected by <a href="https://docs.microsoft.com/windows/desktop//wmformat/wmformat-glossary">DRM</a>.

</td>
</tr>
</table>
 




## -remarks



Stream samples are samples received directly from the source file, and are not decompressed. If you receive compressed samples, you must either keep them compressed, or decompress them with your application. The Windows Media Format SDK does not provide methods to decompress samples once they have been removed from a file.

The application can register itself to receive samples directly from the Windows Media streams rather than letting the reader decompress them first. To do this, the object implementing <a href="https://msdn.microsoft.com/69b897a8-cc26-445d-9d41-b917b399fb14">IWMReaderCallback</a> (supplied by the application) must support <a href="https://msdn.microsoft.com/9d18961a-5ea4-4f3e-b473-7399e155f800">IWMReaderCallbackAdvanced</a>. To determine which streams are in an ASF file, and what their stream numbers are, call <b>QueryInterface</b> using the reader object to access the <a href="https://msdn.microsoft.com/00f28d6b-d27d-4268-960e-c8ea25e5359e">IWMProfile</a> interface, and examine the streams in the profile.




## -see-also




<a href="https://msdn.microsoft.com/a7a20f87-6f21-4fe8-8889-1b6689daf833">IWMReaderAdvanced Interface</a>



<a href="https://msdn.microsoft.com/cdb76a25-fc30-4be2-a54e-928050699e58">IWMReaderAdvanced::GetReceiveStreamSamples</a>
 

 

