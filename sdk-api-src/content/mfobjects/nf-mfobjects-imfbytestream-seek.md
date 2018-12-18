---
UID: NF:mfobjects.IMFByteStream.Seek
title: IMFByteStream::Seek
author: windows-sdk-content
description: Moves the current position in the stream by a specified offset.
old-location: mf\imfbytestream_seek.htm
tech.root: medfound
ms.assetid: 512c67a5-e87d-4a81-8577-e64dac868c40
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 512c67a5-e87d-4a81-8577-e64dac868c40, IMFByteStream interface [Media Foundation],Seek method, IMFByteStream.Seek, IMFByteStream::Seek, MFBYTESTREAM_SEEK_FLAG_CANCEL_PENDING_IO, Seek, Seek method [Media Foundation], Seek method [Media Foundation],IMFByteStream interface, mf.imfbytestream_seek, mfobjects/IMFByteStream::Seek
ms.topic: method
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFByteStream.Seek
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFByteStream::Seek


## -description



Moves the current position in the stream by a specified offset.




## -parameters




### -param SeekOrigin [in]

Specifies the origin of the seek as a member of the <a href="https://msdn.microsoft.com/ad7ad61a-0c02-4a8f-96c3-33f7d1f0ce51">MFBYTESTREAM_SEEK_ORIGIN</a> enumeration. The offset is calculated relative to this position.
          


### -param llSeekOffset [in]

Specifies the new position, as a byte offset from the seek origin.
          


### -param dwSeekFlags [in]

Specifies zero or more flags. The following flags are defined.
          

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MFBYTESTREAM_SEEK_FLAG_CANCEL_PENDING_IO"></a><a id="mfbytestream_seek_flag_cancel_pending_io"></a><dl>
<dt><b>MFBYTESTREAM_SEEK_FLAG_CANCEL_PENDING_IO</b></dt>
</dl>
</td>
<td width="60%">
All pending I/O requests are canceled after the seek request completes successfully.
              

</td>
</tr>
</table>
 


### -param pqwCurrentPosition [out]

Receives the new position after the seek.
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>
<b> Implementation notes:</b> This method should update the current position in the stream by adding the <i>qwSeekOffset</i> to the seek <i>SeekOrigin</i> position. This should be the same value passed back in the <i>pqwCurrentPosition</i> parameter. 
Other methods that can update the current position are <a href="https://msdn.microsoft.com/6e0d5363-f2c2-4334-86ca-71fac61073d3">Read</a>, <a href="https://msdn.microsoft.com/ed4aaf2a-270c-4518-b04d-cdac966bf9a5">BeginRead</a>, <a href="https://msdn.microsoft.com/d1f1195a-b6ee-441c-af8b-fce3dc163e95">Write</a>, <a href="https://msdn.microsoft.com/078a8ffe-7b4f-487e-8655-fe5ea14ba306">BeginWrite</a>, and <a href="https://msdn.microsoft.com/20518fed-4083-413b-b9b1-e54c4c5630d4">SetCurrentPosition</a>.





## -see-also




<a href="https://msdn.microsoft.com/690035b7-2855-4714-938f-f8250ec70d24">IMFByteStream</a>
 

 

