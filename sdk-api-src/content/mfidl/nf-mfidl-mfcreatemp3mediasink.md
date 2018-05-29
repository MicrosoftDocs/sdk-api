---
UID: NF:mfidl.MFCreateMP3MediaSink
title: MFCreateMP3MediaSink function
author: windows-sdk-content
description: Creates the MP3 media sink.
old-location: mf\mfcreatemp3mediasink.htm
old-project: medfound
ms.assetid: b555e9c8-5a2a-452d-8edf-c41c0e24296b
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: MFCreateMP3MediaSink, MFCreateMP3MediaSink function [Media Foundation], mf.mfcreatemp3mediasink, mfidl/MFCreateMP3MediaSink
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MFSensorDeviceMode
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	mf.dll
api_name:
-	MFCreateMP3MediaSink
product: Windows
targetos: Windows
req.lib: Mf.lib
req.dll: Mf.dll
req.irql: 
req.product: GDI+ 1.1
---

# MFCreateMP3MediaSink function


## -description


Creates the MP3 media sink.


## -parameters




### -param pTargetByteStream [in]

A pointer to the <a href="https://msdn.microsoft.com/690035b7-2855-4714-938f-f8250ec70d24">IMFByteStream</a> interface of a byte stream.  The media sink writes the MP3 file to this byte stream. The byte stream must be writable.


### -param ppMediaSink [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/103e6fd8-a18f-480a-8261-099623014659">IMFMediaSink</a> interface of the MP3 media sink.. The caller must release the interface.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




        The MP3  media sink takes compressed MP3
audio samples as input, and writes an MP3 file with ID3 headers as output. The MP3 media sink does not perform MP3 audio encoding.
      


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT CreateMP3Sink(PCWSTR pszOutputFile, IMFMediaSink **ppSink)
{
    *ppSink = NULL;

    IMFByteStream* pStream = NULL;

    // Create a byte stream for the output file.
    HRESULT hr =  MFCreateFile(
        MF_ACCESSMODE_WRITE, 
        MF_OPENMODE_DELETE_IF_EXIST, 
        MF_FILEFLAGS_NONE, 
        pszOutputFile, 
        &amp;pStream
        );
       
    // Create the MP3 media sink.
    if (SUCCEEDED(hr))
    {
        hr =  MFCreateMP3MediaSink(pStream, ppSink);
    }

    SafeRelease(&amp;pStream);
    return hr;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

