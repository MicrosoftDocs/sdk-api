---
UID: NF:wmsdkidl.IWMWriter.BeginWriting
title: IWMWriter::BeginWriting (wmsdkidl.h)
author: windows-sdk-content
description: The BeginWriting method initializes the writing process.
old-location: wmformat\iwmwriter_beginwriting.htm
tech.root: wmformat
ms.assetid: df511ff0-a87b-442a-85bd-c8d924ab2047
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: BeginWriting, BeginWriting method [windows Media Format], BeginWriting method [windows Media Format],IWMWriter interface, IWMWriter interface [windows Media Format],BeginWriting method, IWMWriter.BeginWriting, IWMWriter::BeginWriting, IWMWriterBeginWriting, wmformat.iwmwriter_beginwriting, wmsdkidl/IWMWriter::BeginWriting
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
 - IWMWriter.BeginWriting
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMWriter::BeginWriting


## -description



The <b>BeginWriting</b> method initializes the writing process.




## -parameters






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
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_AUDIO_CODEC_ERROR</b></dt>
</dl>
</td>
<td width="60%">
An error occurred in the audio codec.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_AUDIO_CODEC_NOT_INSTALLED</b></dt>
</dl>
</td>
<td width="60%">
The required audio codec is not available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_DRM_RIV_TOO_SMALL</b></dt>
</dl>
</td>
<td width="60%">
A more recent content revocation list is needed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_INVALID_OUTPUT_FORMAT</b></dt>
</dl>
</td>
<td width="60%">
The output format is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_VIDEO_CODEC_ERROR</b></dt>
</dl>
</td>
<td width="60%">
An error occurred in the video codec.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_VIDEO_CODEC_NOT_INSTALLED</b></dt>
</dl>
</td>
<td width="60%">
The required video codec is not available.

</td>
</tr>
</table>
 




## -remarks



The <b>BeginWriting</b> method must be called before any samples are written. This method does not actually start writing, but initializes the process. Between this call and the call to <a href="https://msdn.microsoft.com/en-us/library/Dd757475(v=VS.85).aspx">EndWriting</a> there can be no configuration changes to the writer. The <b>EndWriting</b> method must be called to cleanly end the writing of the samples.

The following operations can be performed only before calling <b>BeginWriting</b>:

<ul>
<li>Setting the profile with <a href="https://msdn.microsoft.com/en-us/library/Dd757507(v=VS.85).aspx">SetProfile</a>
</li>
<li>Setting the output filename (if using <a href="https://msdn.microsoft.com/en-us/library/Dd757506(v=VS.85).aspx">IWMWriter::SetOutputFilename</a>)</li>
<li>Setting an attribute with <a href="https://msdn.microsoft.com/en-us/library/Dd798527(v=VS.85).aspx">IWMHeaderInfo::SetAttribute</a>
</li>
<li><a href="https://msdn.microsoft.com/en-us/library/Dd757828(v=VS.85).aspx">Marker</a> operations (<a href="https://msdn.microsoft.com/en-us/library/Dd798522(v=VS.85).aspx">IWMHeaderInfo::GetMarkerCount</a>, <a href="https://msdn.microsoft.com/en-us/library/Dd798521(v=VS.85).aspx">GetMarker</a>, <a href="https://msdn.microsoft.com/en-us/library/Dd798516(v=VS.85).aspx">AddMarker</a>, and <a href="https://msdn.microsoft.com/en-us/library/Dd798525(v=VS.85).aspx">RemoveMarker</a>, although <b>AddMarker</b> is not implemented on the writer and the rest aren't useful if there are no markers)</li>
<li>Calling <a href="https://msdn.microsoft.com/en-us/library/Dd757484(v=VS.85).aspx">IWMWriter::SetInputProps</a> with a <b>NULL</b><a href="https://msdn.microsoft.com/en-us/library/Dd757209(v=VS.85).aspx">IWMInputMediaProps</a> parameter to indicate that the input stream will be written using <a href="https://msdn.microsoft.com/en-us/library/Dd798741(v=VS.85).aspx">WriteStreamSample</a>.</li>
<li>Header Script operations (<a href="https://msdn.microsoft.com/en-us/library/Dd798524(v=VS.85).aspx">IWMHeaderInfo::GetScriptCount</a>, <a href="https://msdn.microsoft.com/en-us/library/Dd798523(v=VS.85).aspx">GetScript</a>, <a href="https://msdn.microsoft.com/en-us/library/Dd798517(v=VS.85).aspx">AddScript</a>, and <a href="https://msdn.microsoft.com/en-us/library/Dd798526(v=VS.85).aspx">RemoveScript</a>)</li>
<li>Codec info operations (<a href="https://msdn.microsoft.com/en-us/library/Dd798507(v=VS.85).aspx">IWMHeaderInfo2::GetCodecInfoCount</a> and <a href="https://msdn.microsoft.com/en-us/library/Dd798506(v=VS.85).aspx">GetCodecInfo</a>)</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Dd798782(v=VS.85).aspx">IWMWriterPostView::SetPostViewProps</a>
</li>
</ul>
The following methods can be called only after a profile has been set and before calling <b>BeginWriting</b>:<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Dd798520(v=VS.85).aspx">IWMHeaderInfo::GetAttributeCount</a>
</li>
<li>
<a href="https://msdn.microsoft.com/905fdf2c-a398-457e-80e9-aac124301f99">IWMHeaderInfo::GetAttributeByIndex</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Dd798519(v=VS.85).aspx">IWMHeaderInfo::GetAttributeByName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Dd798723(v=VS.85).aspx">IWMWriterAdvanced2::SetInputSetting</a>
</li>
</ul>


Note: <a href="https://msdn.microsoft.com/en-us/library/Dd798723(v=VS.85).aspx">SetInputSetting</a> can be called after <b>BeginWriting</b> for g_wszDeinterlaceMode, g_wszInitialPatternForInverseTelecine, g_wszInterlacedCoding, and g_wszJPEGCompressionQuality.

The following operations can be performed any time after a profile has been set:

<ul>
<li>Any postview operations except for <b>SetPostViewProps</b></li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Dd757484(v=VS.85).aspx">IWMWriter::SetInputProps</a> except when passing in a <b>NULL</b><a href="https://msdn.microsoft.com/en-us/library/Dd757209(v=VS.85).aspx">IWMInputMediaProps</a> parameter.</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Dd757482(v=VS.85).aspx">IWMWriter::GetInputProps</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Dd757480(v=VS.85).aspx">IWMWriter::GetInputFormatCount</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Dd757478(v=VS.85).aspx">IWMWriter::GetInputFormat</a>
</li>
</ul>
The following operations can be performed only after calling <b>BeginWriting</b>:

<ul>
<li>Allocating samples with <a href="https://msdn.microsoft.com/en-us/library/Dd757473(v=VS.85).aspx">IWMWriter::AllocateSample</a>
</li>
<li>Writing samples with <a href="https://msdn.microsoft.com/en-us/library/Dd757509(v=VS.85).aspx">IWMWriter::WriteSample</a> and <a href="https://msdn.microsoft.com/en-us/library/Dd798741(v=VS.85).aspx">IWMWriterAdvanced::WriteStreamSample</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Dd757475(v=VS.85).aspx">IWMWriter::EndWriting</a>
</li>
</ul>
The following operations can be performed at any time:

<ul>
<li>Adding and removing a sink with <a href="https://msdn.microsoft.com/en-us/library/Dd798727(v=VS.85).aspx">IWMWriterAdvanced::AddSink</a> and <a href="https://msdn.microsoft.com/en-us/library/Dd798736(v=VS.85).aspx">IWMWriterAdvanced::RemoveSink</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Dd798737(v=VS.85).aspx">IWMWriterAdvanced::SetLiveSource</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Dd798734(v=VS.85).aspx">IWMWriterAdvanced::IsRealTime</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Dd798732(v=VS.85).aspx">IWMWriterAdvanced::GetWriterTime</a> (although it won't return meaningful values)</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Dd798730(v=VS.85).aspx">IWMWriterAdvanced::GetStatistics</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Dd798739(v=VS.85).aspx">IWMWriterAdvanced::SetSyncTolerance</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Dd798731(v=VS.85).aspx">IWMWriterAdvanced::GetSyncTolerance</a>
</li>
</ul>

#### Examples

The following example code outlines how to set up a writer and send output both to a network sink and an archive file.


```cpp

IWMWriter *             pWriter = NULL;
IWMWriterAdvanced *     pWriterAdvanced = NULL;
IWMWriterFileSink2 *    pWriterFileSink = NULL;
IWMWriterNetworkSink2 * pWriterNetworkSink = NULL;
HRESULT                 hr = S_OK;
DWORD                   dwPort;

// Do everything in a dummy loop for easy error-handling.

do
{
    // Create the basic objects.

    hr = WMCreateWriter( &pWriter );
    if( FAILED( hr ) )
    {
        break;
    }

    hr = WMCreateWriterFileSink( &pWriterFileSink );
    if( FAILED( hr ) )
    {
        break;
    }

    hr = WMCreateWriterNetworkSink( &pWriterNetworkSink );
    if( FAILED( hr ) )
    {
        break;
    }

    // Retrieve a pointer to an IWMWriterAdvanced interface and add the sinks.

    hr = pWriter->QueryInterface( IID_IWMWriterAdvanced, (void **)&pWriterAdvanced );
    if( FAILED( hr ) )
    {
        break;
    }

    hr = pWriterAdvanced->AddSink( pWriterFileSink );
    if( FAILED( hr ) )
    {
        break;
    }

    hr = pWriterAdvanced->AddSink( pWriterNetworkSink );
    if( FAILED( hr ) )
    {
        break;
    }

    hr = pWriterFileSink->Open( L"Archive file name" );
    if( FAILED( hr ) )
    {
        break;
    }

    // Setting the port number to zero enables the SDK to select an
    // appropriate port number.
    dwPort = 0;
    hr = pWriterNetworkSink->Open( &dwPort );
    if( FAILED( hr ) )
    {
        break;
    }

    hr = pWriter->BeginWriting();
    if( FAILED( hr ) )
    {
        break;
    }

    // Code to send data to the writer goes here (not shown).

    // Close both sinks.
    hr = pWriterFileSink->Close();
    if( FAILED( hr ) )
    {
        break;
    }

    hr = pWriterNetworkSink->Close();
    if( FAILED( hr ) )
    {
        break;
    }

    hr = pWriter-> EndWriting();
    if( FAILED( hr ) )
    {
        break;
    }
}
while( FALSE );

// Clean up.

if ( pWriter )
{
    pWriter->Release();
}
if ( pWriterAdvanced )
{
    pWriterAdvanced->Release();
}
if ( pWriterFileSink )
{
    pWriterFileSink->Release();
}
if ( pWriterNetworkSink )
{
    pWriterNetworkSink->Release();
}

```





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd798719(v=VS.85).aspx">IWMWriter Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd757475(v=VS.85).aspx">IWMWriter::EndWriting</a>
 

 

