---
UID: NF:mfcaptureengine.IMFCaptureRecordSink.SetOutputFileName
title: IMFCaptureRecordSink::SetOutputFileName (mfcaptureengine.h)
author: windows-sdk-content
description: Specifies the name of the output file for the recording.
old-location: mf\imfcapturerecordsink_setoutputfilename.htm
tech.root: medfound
ms.assetid: 96BEE09C-1B17-4857-B0DC-553D14B908E7
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMFCaptureRecordSink interface [Media Foundation],SetOutputFileName method, IMFCaptureRecordSink.SetOutputFileName, IMFCaptureRecordSink::SetOutputFileName, SetOutputFileName, SetOutputFileName method [Media Foundation], SetOutputFileName method [Media Foundation],IMFCaptureRecordSink interface, mf.imfcapturerecordsink_setoutputfilename, mfcaptureengine/IMFCaptureRecordSink::SetOutputFileName
ms.topic: method
req.header: mfcaptureengine.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfcaptureengine.h
api_name:
 - IMFCaptureRecordSink.SetOutputFileName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFCaptureRecordSink::SetOutputFileName


## -description


Specifies the name of the output file for the recording.


## -parameters




### -param fileName [in]

A null-terminated string that contains the URL of the output file. 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The capture engine uses the file name extension to select the container type for the output file. For example, if the file name extension is ."mp4", the capture engine creates an MP4 file.

Calling this method overrides any previous call to <a href="https://msdn.microsoft.com/C33357C8-882A-4350-8638-46C2220FC445">IMFCaptureRecordSink::SetOutputByteStream</a> or <a href="https://msdn.microsoft.com/1D7BB0D1-3F77-4AF3-9624-73EE4D0D0BCE">IMFCaptureRecordSink::SetSampleCallback</a>.




## -see-also




<a href="https://msdn.microsoft.com/AEF5923D-C4ED-4BEA-A969-163ED837A5BD">IMFCaptureRecordSink</a>
 

 

