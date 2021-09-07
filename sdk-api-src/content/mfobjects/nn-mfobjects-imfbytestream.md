---
UID: NN:mfobjects.IMFByteStream
title: IMFByteStream (mfobjects.h)
description: Represents a byte stream from some data source, which might be a local file, a network file, or some other source.
helpviewer_keywords: ["690035b7-2855-4714-938f-f8250ec70d24","IMFByteStream","IMFByteStream interface [Media Foundation]","IMFByteStream interface [Media Foundation]","described","mf.imfbytestream","mfobjects/IMFByteStream"]
old-location: mf\imfbytestream.htm
tech.root: mf
ms.assetid: 690035b7-2855-4714-938f-f8250ec70d24
ms.date: 12/05/2018
ms.keywords: 690035b7-2855-4714-938f-f8250ec70d24, IMFByteStream, IMFByteStream interface [Media Foundation], IMFByteStream interface [Media Foundation],described, mf.imfbytestream, mfobjects/IMFByteStream
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFByteStream
 - mfobjects/IMFByteStream
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFByteStream
---

# IMFByteStream interface


## -description

Represents a byte stream from some data source, which might be a local file, a network file, or some other source. The <b>IMFByteStream</b> interface supports the typical stream operations, such as reading, writing, and seeking.

## -inheritance

The <b>IMFByteStream</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFByteStream</b> also has these types of members:

## -remarks

The following functions return <b>IMFByteStream</b> pointers for local files:
        

<ul>
<li>
<a href="/windows/desktop/api/mfapi/nf-mfapi-mfbegincreatefile">MFBeginCreateFile</a>
</li>
<li>
<a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreatefile">MFCreateFile</a>
</li>
<li>
<a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreatetempfile">MFCreateTempFile</a>
</li>
</ul>
A byte stream for a media source can be opened with read access. A byte stream for an archive media sink should be opened with both read and write access. (Read access may be required, because the archive sink might need to read portions of the file as it writes.)
      

Some implementations of this interface also expose one or more of the following interfaces:

<ul>
<li>
<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a>
</li>
<li>
<a href="/windows/desktop/api/mfidl/nn-mfidl-imfbytestreambuffering">IMFByteStreamBuffering</a>
</li>
<li>
<a href="/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamcachecontrol">IMFByteStreamCacheControl</a>
</li>
<li>
<a href="/windows/desktop/api/mfidl/nn-mfidl-imfgetservice">IMFGetService</a>
</li>
<li>
<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator">IMFMediaEventGenerator</a>
</li>
</ul>
This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/medfound/byte-stream-attributes">Byte Stream Attributes</a>



<a href="/windows/desktop/api/mfidl/nn-mfidl-imfbytestreambuffering">IMFByteStreamBuffering</a>



<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
