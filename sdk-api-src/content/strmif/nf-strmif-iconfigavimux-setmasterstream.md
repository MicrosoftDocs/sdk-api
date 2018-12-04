---
UID: NF:strmif.IConfigAviMux.SetMasterStream
title: IConfigAviMux::SetMasterStream
author: windows-sdk-content
description: The SetMasterStream method specifies a stream that will be used to synchronize the other streams in the file.
old-location: dshow\iconfigavimux_setmasterstream.htm
tech.root: DirectShow
ms.assetid: 1f255498-8bbb-48a0-ae97-0cf2698e609b
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IConfigAviMux interface [DirectShow],SetMasterStream method, IConfigAviMux.SetMasterStream, IConfigAviMux::SetMasterStream, IConfigAviMuxSetMasterStream, SetMasterStream, SetMasterStream method [DirectShow], SetMasterStream method [DirectShow],IConfigAviMux interface, dshow.iconfigavimux_setmasterstream, strmif/IConfigAviMux::SetMasterStream
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IConfigAviMux.SetMasterStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IConfigAviMux::SetMasterStream


## -description



The <code>SetMasterStream</code> method specifies a stream that will be used to synchronize the other streams in the file.




## -parameters




### -param iStream [in]

Specifies the index of the stream, or –1 to indicate no master stream. The AVI Mux writes one stream for each connected input pin. Stream numbers are indexed from zero.


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
</table>
 




## -remarks



If you are capturing audio and video from two different sources, use this method to synchronize the streams. Streams coming from separate capture sources may be captured at slightly different rates. If you specify a master stream, the AVI Mux adjusts the playback rates for the other streams, to compensate for any drift that might occur.

It is recommended to use the audio stream as the master stream, because minor adjustments to the video playback rate are less noticeable than changes to the audio playback rate. Also, modifying the audio playback rate will cause the audio to be resampled by the audio driver.

This method works by adjusting the <i>dwScale</i> and <i>dwRate</i> values in the <a href="https://msdn.microsoft.com/f07c28ac-2dd0-428a-a94a-32aec2bb0854">AVISTREAMHEADER</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/2d8cf5be-1252-4b58-89b1-f5c53ea17d0e">AVI RIFF File Reference</a>



<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/4cc3cdeb-ebc5-46e1-8cc4-84b40e91323b">IConfigAviMux Interface</a>
 

 

