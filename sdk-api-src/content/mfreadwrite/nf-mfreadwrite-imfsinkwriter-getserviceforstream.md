---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IMFSinkWriter::GetServiceForStream


## -description


Queries the underlying media sink or encoder for an interface.


## -parameters




### -param dwStreamIndex [in]

The zero-based index of a stream to query, or <b>MF_SINK_WRITER_MEDIASINK</b> to query the media sink itself.


### -param guidService [in]

A service identifier GUID, or <b>GUID_NULL</b>.  If the value is <b>GUID_NULL</b>, the method calls <b>QueryInterface</b> to get the requested interface. Otherwise, the method calls <a href="https://msdn.microsoft.com/4287dd1f-1718-4231-bc62-b58e0e61d688">IMFGetService::GetService</a>. For a list of service identifiers, see <a href="https://msdn.microsoft.com/264a0e86-49e9-4777-956b-a83e9db52a25">Service Interfaces</a>.


### -param riid [in]

The interface identifier (IID) of the interface being requested.




### -param ppvObject [out]

Receives a pointer to the requested interface. The caller must release the interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If the <i>dwStreamIndex</i> parameter equals <b>MF_SINK_WRITER_MEDIASINK</b>, the method attempts to get the interface from the media sink. Otherwise, it attempts to get the interface from the encoder for the stream at the specified index. If that fails, or if no encoder is present, the method attempts to get the interface from the stream on the media sink.


          If the input and output types of the sink are identical and compressed,
          it's possible that no encoding is required and the video encoder will not be instantiated.
          In that case, <b>GetServiceForStream</b> will return MF_E_UNSUPPORTED_SERVICE.
        

This interface is available on Windows Vista if Platform Update Supplement for Windows Vista is installed.




## -see-also




<a href="https://msdn.microsoft.com/76fb915e-1586-429a-88a5-bd1290799352">IMFSinkWriter</a>



<a href="https://msdn.microsoft.com/23AF25B8-B94C-48BC-83D8-5863ACFFD4CA">Sink Writer</a>
 

 

