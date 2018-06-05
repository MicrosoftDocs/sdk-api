---
UID: NF:mfidl.MFCreateTranscodeTopologyFromByteStream
title: MFCreateTranscodeTopologyFromByteStream function
author: windows-sdk-content
description: Creates a topology for transcoding to a byte stream.
old-location: mf\mfcreatetranscodetopologyfrombytestream.htm
old-project: medfound
ms.assetid: FBA9E0A1-7763-4566-8245-D626C82D0355
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: MFCreateTranscodeTopologyFromByteStream, MFCreateTranscodeTopologyFromByteStream function [Media Foundation], mf.mfcreatetranscodetopologyfrombytestream, mfidl/MFCreateTranscodeTopologyFromByteStream
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: MFSensorDeviceMode
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	mf.dll
api_name:
-	MFCreateTranscodeTopologyFromByteStream
product: Windows
targetos: Windows
req.lib: Mf.lib
req.dll: Mf.dll
req.irql: 
req.product: GDI+ 1.1
---

# MFCreateTranscodeTopologyFromByteStream function


## -description


Creates a topology for transcoding to a byte stream.


## -parameters




### -param pSrc [in]

A pointer to the <a href="https://msdn.microsoft.com/8b579f61-6fea-4b20-a051-7633fc01fa05">IMFMediaSource</a> interface of a media source. The media source provides that source content for transcoding.


### -param pOutputStream [in]

A pointer to the <a href="https://msdn.microsoft.com/690035b7-2855-4714-938f-f8250ec70d24">IMFByteStream</a> interface of a byte stream. The transcoded output will be written to this byte stream.


### -param pProfile [in]

A pointer to the <a href="https://msdn.microsoft.com/82e012e0-84d8-4791-8b6f-bda58b498a90">IMFTranscodeProfile</a> interface of a transcoding profile. 


### -param ppTranscodeTopo [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/f293e9ee-9bd2-4b3e-a4ff-53457ee910f6">IMFTopology</a> interface. The caller must release the interface.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This function creates a partial topology that contains the media source, the encoder, and the media sink. 




## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>



<a href="https://msdn.microsoft.com/dac99908-be90-415d-8837-2f97d573feb5">Media Session</a>



<a href="https://msdn.microsoft.com/6fc19244-0f42-4d23-899d-c79e97018855">Topologies</a>
 

 

