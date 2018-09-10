---
UID: NF:wmsdkidl.IWMWriter.BeginWriting
title: IWMWriter::BeginWriting
author: windows-sdk-content
description: The BeginWriting method initializes the writing process.
old-location: wmformat\iwmwriter_beginwriting.htm
tech.root: wmformat
ms.assetid: df511ff0-a87b-442a-85bd-c8d924ab2047
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: BeginWriting, BeginWriting method [windows Media Format], BeginWriting method [windows Media Format],IWMWriter interface, IWMWriter interface [windows Media Format],BeginWriting method, IWMWriter.BeginWriting, IWMWriter::BeginWriting, IWMWriterBeginWriting, wmformat.iwmwriter_beginwriting, wmsdkidl/IWMWriter::BeginWriting
ms.prod: windows-hardware
ms.technology: windows-devices
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



The <b>BeginWriting</b> method must be called before any samples are written. This method does not actually start writing, but initializes the process. Between this call and the call to <a href="https://msdn.microsoft.com/020e2c9d-9581-48c9-bc7b-a0e9e5a60c63">EndWriting</a> there can be no configuration changes to the writer. The <b>EndWriting</b> method must be called to cleanly end the writing of the samples.

The following operations can be performed only before calling <b>BeginWriting</b>:

<ul>
<li>Setting the profile with <a href="https://msdn.microsoft.com/1a931896-c102-4b3b-a5a3-b3ef85b276b9">SetProfile</a>
</li>
<li>Setting the output filename (if using <a href="https://msdn.microsoft.com/352cf497-f7d6-41e8-bdbb-c59215b617a3">IWMWriter::SetOutputFilename</a>)</li>
<li>Setting an attribute with <a href="https://msdn.microsoft.com/174969a2-4fe2-477b-9990-051d23bf8a29">IWMHeaderInfo::SetAttribute</a>
</li>
<li><a href="https://msdn.microsoft.com/en-us/library/Dd757828(v=VS.85).aspx">Marker</a> operations (<a href="https://msdn.microsoft.com/c0d8e61d-8703-407a-9610-9e9f29ab92a1">IWMHeaderInfo::GetMarkerCount</a>, <a href="https://msdn.microsoft.com/ae035991-86c8-4ffc-b819-5a5ce81a980f">GetMarker</a>, <a href="https://msdn.microsoft.com/cfa111bb-7bbb-448a-b2db-d36637c01a52">AddMarker</a>, and <a href="https://msdn.microsoft.com/b95aa113-b218-44ef-9516-20894e02ee6c">RemoveMarker</a>, although <b>AddMarker</b> is not implemented on the writer and the rest aren't useful if there are no markers)</li>
<li>Calling <a href="https://msdn.microsoft.com/15084a4d-06e8-4f74-9697-ced794d2cdae">IWMWriter::SetInputProps</a> with a <b>NULL</b><a href="https://msdn.microsoft.com/d901ac66-d4b3-4256-bd7b-53cccb3de644">IWMInputMediaProps</a> parameter to indicate that the input stream will be written using <a href="https://msdn.microsoft.com/498bfb73-bfa5-429d-ae8a-3a691fc25fc2">WriteStreamSample</a>.</li>
<li>Header Script operations (<a href="https://msdn.microsoft.com/c1a0b35c-db05-402a-9bde-684bead1eedf">IWMHeaderInfo::GetScriptCount</a>, <a href="https://msdn.microsoft.com/779a7618-9f22-4caf-8a4e-b622e422c30d">GetScript</a>, <a href="https://msdn.microsoft.com/e20644fb-077e-4eee-8802-6099002f3969">AddScript</a>, and <a href="https://msdn.microsoft.com/c66e808d-25f9-4745-8bcc-731f2556f470">RemoveScript</a>)</li>
<li>Codec info operations (<a href="https://msdn.microsoft.com/1f77f362-5cc7-4d12-9b5f-0436d490b46d">IWMHeaderInfo2::GetCodecInfoCount</a> and <a href="https://msdn.microsoft.com/685eaf9e-6cc8-4c38-be34-afa4b504a326">GetCodecInfo</a>)</li>
<li>
<a href="https://msdn.microsoft.com/e5b92065-fff3-41d2-b263-375ae14869e5">IWMWriterPostView::SetPostViewProps</a>
</li>
</ul>
The following methods can be called only after a profile has been set and before calling <b>BeginWriting</b>:<ul>
<li>
<a href="https://msdn.microsoft.com/d5f0be62-4f15-45ca-8593-f5703a1f932a">IWMHeaderInfo::GetAttributeCount</a>
</li>
<li>
<a href="https://msdn.microsoft.com/905fdf2c-a398-457e-80e9-aac124301f99">IWMHeaderInfo::GetAttributeByIndex</a>
</li>
<li>
<a href="https://msdn.microsoft.com/8941b989-f052-4e61-a64a-06748947fcf4">IWMHeaderInfo::GetAttributeByName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/a920bfe8-1f95-4957-b6c4-9749d5e10ee3">IWMWriterAdvanced2::SetInputSetting</a>
</li>
</ul>


Note: <a href="https://msdn.microsoft.com/a920bfe8-1f95-4957-b6c4-9749d5e10ee3">SetInputSetting</a> can be called after <b>BeginWriting</b> for g_wszDeinterlaceMode, g_wszInitialPatternForInverseTelecine, g_wszInterlacedCoding, and g_wszJPEGCompressionQuality.

The following operations can be performed any time after a profile has been set:

<ul>
<li>Any postview operations except for <b>SetPostViewProps</b></li>
<li>
<a href="https://msdn.microsoft.com/15084a4d-06e8-4f74-9697-ced794d2cdae">IWMWriter::SetInputProps</a> except when passing in a <b>NULL</b><a href="https://msdn.microsoft.com/d901ac66-d4b3-4256-bd7b-53cccb3de644">IWMInputMediaProps</a> parameter.</li>
<li>
<a href="https://msdn.microsoft.com/2889a1a7-3111-4c13-b15a-659f519c22f6">IWMWriter::GetInputProps</a>
</li>
<li>
<a href="https://msdn.microsoft.com/c3afe9e8-e045-4329-b3e5-6026147322ad">IWMWriter::GetInputFormatCount</a>
</li>
<li>
<a href="https://msdn.microsoft.com/c058de81-a29a-4bcd-a819-3cdef11cae9f">IWMWriter::GetInputFormat</a>
</li>
</ul>
The following operations can be performed only after calling <b>BeginWriting</b>:

<ul>
<li>Allocating samples with <a href="https://msdn.microsoft.com/b23b2364-fb36-479f-bf92-76a5bb4722de">IWMWriter::AllocateSample</a>
</li>
<li>Writing samples with <a href="https://msdn.microsoft.com/ba1cf121-1d01-4e90-9ab0-95af0b6e3850">IWMWriter::WriteSample</a> and <a href="https://msdn.microsoft.com/498bfb73-bfa5-429d-ae8a-3a691fc25fc2">IWMWriterAdvanced::WriteStreamSample</a>
</li>
<li>
<a href="https://msdn.microsoft.com/020e2c9d-9581-48c9-bc7b-a0e9e5a60c63">IWMWriter::EndWriting</a>
</li>
</ul>
The following operations can be performed at any time:

<ul>
<li>Adding and removing a sink with <a href="https://msdn.microsoft.com/65763ac3-fba0-4de6-9c2e-4e241bbe5f13">IWMWriterAdvanced::AddSink</a> and <a href="https://msdn.microsoft.com/e2fc7f82-981a-4f69-b99d-71514ed2c6ae">IWMWriterAdvanced::RemoveSink</a>
</li>
<li>
<a href="https://msdn.microsoft.com/ab015f92-498e-44c7-95c9-869dfdfccc09">IWMWriterAdvanced::SetLiveSource</a>
</li>
<li>
<a href="https://msdn.microsoft.com/3d00eb78-d90e-41a0-9bba-305ac65057f3">IWMWriterAdvanced::IsRealTime</a>
</li>
<li>
<a href="https://msdn.microsoft.com/ed15e545-8b37-4098-8e2f-96f4cfb271d3">IWMWriterAdvanced::GetWriterTime</a> (although it won't return meaningful values)</li>
<li>
<a href="https://msdn.microsoft.com/005c2039-e821-42ab-bead-1bf40f2ab171">IWMWriterAdvanced::GetStatistics</a>
</li>
<li>
<a href="https://msdn.microsoft.com/d60020bf-52f1-46a0-aeae-367e3b179fac">IWMWriterAdvanced::SetSyncTolerance</a>
</li>
<li>
<a href="https://msdn.microsoft.com/f62d3405-3125-4df6-bd06-fa70358560ad">IWMWriterAdvanced::GetSyncTolerance</a>
</li>
</ul>

#### Examples

The following example code outlines how to set up a writer and send output both to a network sink and an archive file.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
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

    hr = WMCreateWriter( &amp;pWriter );
    if( FAILED( hr ) )
    {
        break;
    }

    hr = WMCreateWriterFileSink( &amp;pWriterFileSink );
    if( FAILED( hr ) )
    {
        break;
    }

    hr = WMCreateWriterNetworkSink( &amp;pWriterNetworkSink );
    if( FAILED( hr ) )
    {
        break;
    }

    // Retrieve a pointer to an IWMWriterAdvanced interface and add the sinks.

    hr = pWriter-&gt;QueryInterface( IID_IWMWriterAdvanced, (void **)&amp;pWriterAdvanced );
    if( FAILED( hr ) )
    {
        break;
    }

    hr = pWriterAdvanced-&gt;AddSink( pWriterFileSink );
    if( FAILED( hr ) )
    {
        break;
    }

    hr = pWriterAdvanced-&gt;AddSink( pWriterNetworkSink );
    if( FAILED( hr ) )
    {
        break;
    }

    hr = pWriterFileSink-&gt;Open( L"Archive file name" );
    if( FAILED( hr ) )
    {
        break;
    }

    // Setting the port number to zero enables the SDK to select an
    // appropriate port number.
    dwPort = 0;
    hr = pWriterNetworkSink-&gt;Open( &amp;dwPort );
    if( FAILED( hr ) )
    {
        break;
    }

    hr = pWriter-&gt;BeginWriting();
    if( FAILED( hr ) )
    {
        break;
    }

    // Code to send data to the writer goes here (not shown).

    // Close both sinks.
    hr = pWriterFileSink-&gt;Close();
    if( FAILED( hr ) )
    {
        break;
    }

    hr = pWriterNetworkSink-&gt;Close();
    if( FAILED( hr ) )
    {
        break;
    }

    hr = pWriter-&gt; EndWriting();
    if( FAILED( hr ) )
    {
        break;
    }
}
while( FALSE );

// Clean up.

if ( pWriter )
{
    pWriter-&gt;Release();
}
if ( pWriterAdvanced )
{
    pWriterAdvanced-&gt;Release();
}
if ( pWriterFileSink )
{
    pWriterFileSink-&gt;Release();
}
if ( pWriterNetworkSink )
{
    pWriterNetworkSink-&gt;Release();
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/a194ef11-5203-4e85-af91-cdce0c53fe76">IWMWriter Interface</a>



<a href="https://msdn.microsoft.com/020e2c9d-9581-48c9-bc7b-a0e9e5a60c63">IWMWriter::EndWriting</a>
 

 

