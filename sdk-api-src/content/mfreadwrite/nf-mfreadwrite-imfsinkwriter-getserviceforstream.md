---
UID: NF:mfreadwrite.IMFSinkWriter.GetServiceForStream
title: IMFSinkWriter::GetServiceForStream (mfreadwrite.h)
description: Queries the underlying media sink or encoder for an interface.
helpviewer_keywords: ["GetServiceForStream","GetServiceForStream method [Media Foundation]","GetServiceForStream method [Media Foundation]","IMFSinkWriter interface","IMFSinkWriter interface [Media Foundation]","GetServiceForStream method","IMFSinkWriter.GetServiceForStream","IMFSinkWriter::GetServiceForStream","mf.imfsinkwriter_getserviceforstream","mfreadwrite/IMFSinkWriter::GetServiceForStream"]
old-location: mf\imfsinkwriter_getserviceforstream.htm
tech.root: mf
ms.assetid: 166f8f71-e52d-43b1-9137-e4bf79bf5421
ms.date: 12/05/2018
ms.keywords: GetServiceForStream, GetServiceForStream method [Media Foundation], GetServiceForStream method [Media Foundation],IMFSinkWriter interface, IMFSinkWriter interface [Media Foundation],GetServiceForStream method, IMFSinkWriter.GetServiceForStream, IMFSinkWriter::GetServiceForStream, mf.imfsinkwriter_getserviceforstream, mfreadwrite/IMFSinkWriter::GetServiceForStream
req.header: mfreadwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista and Platform Update Supplement for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFSinkWriter::GetServiceForStream
 - mfreadwrite/IMFSinkWriter::GetServiceForStream
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfreadwrite.h
api_name:
 - IMFSinkWriter.GetServiceForStream
---

# IMFSinkWriter::GetServiceForStream


## -description

Queries the underlying media sink or encoder for an interface.

## -parameters

### -param dwStreamIndex [in]

The zero-based index of a stream to query, or <b>MF_SINK_WRITER_MEDIASINK</b> to query the media sink itself.

### -param guidService [in]

A service identifier GUID, or <b>GUID_NULL</b>.  If the value is <b>GUID_NULL</b>, the method calls <b>QueryInterface</b> to get the requested interface. Otherwise, the method calls <a href="/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice">IMFGetService::GetService</a>. For a list of service identifiers, see <a href="/windows/desktop/medfound/service-interfaces">Service Interfaces</a>.

### -param riid [in]

The interface identifier (IID) of the interface being requested.

### -param ppvObject [out]

Receives a pointer to the requested interface. The caller must release the interface.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If the <i>dwStreamIndex</i> parameter equals <b>MF_SINK_WRITER_MEDIASINK</b>, the method attempts to get the interface from the media sink. Otherwise, it attempts to get the interface from the encoder for the stream at the specified index. If that fails, or if no encoder is present, the method attempts to get the interface from the stream on the media sink.

If the input and output types of the sink are identical and compressed,
          it's possible that no encoding is required and the video encoder will not be instantiated.
          In that case, <b>GetServiceForStream</b> will return MF_E_UNSUPPORTED_SERVICE.
        

This interface is available on Windows Vista if Platform Update Supplement for Windows Vista is installed.

## -see-also

<a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriter">IMFSinkWriter</a>



<a href="/windows/desktop/medfound/sink-writer">Sink Writer</a>