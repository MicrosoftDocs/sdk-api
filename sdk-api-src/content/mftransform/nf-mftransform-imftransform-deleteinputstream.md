---
UID: NF:mftransform.IMFTransform.DeleteInputStream
title: IMFTransform::DeleteInputStream
author: windows-sdk-content
description: Removes an input stream from this Media Foundation transform (MFT).
old-location: mf\imftransform_deleteinputstream.htm
old-project: medfound
ms.assetid: cba37f7f-6ab2-469c-95c2-61d9e4d31d0b
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: DeleteInputStream, DeleteInputStream method [Media Foundation], DeleteInputStream method [Media Foundation],IMFTransform interface, IMFTransform interface [Media Foundation],DeleteInputStream method, IMFTransform.DeleteInputStream, IMFTransform::DeleteInputStream, cba37f7f-6ab2-469c-95c2-61d9e4d31d0b, mf.imftransform_deleteinputstream, mftransform/IMFTransform::DeleteInputStream
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mftransform.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfuuid.lib
-	mfuuid.dll
api_name:
-	IMFTransform.DeleteInputStream
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFTransform::DeleteInputStream


## -description



          Removes an input stream from this Media Foundation transform (MFT).
        


## -parameters




### -param dwStreamID [in]


            Identifier of the input stream to remove.
          


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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">

                The transform has a fixed number of input streams.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDREQUEST</b></dt>
</dl>
</td>
<td width="60%">

                The stream is not removable, or the transform currently has the minimum number of input streams it can support.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDSTREAMNUMBER</b></dt>
</dl>
</td>
<td width="60%">

                Invalid stream identifier.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_TRANSFORM_INPUT_REMAINING</b></dt>
</dl>
</td>
<td width="60%">

                The transform has unprocessed input buffers for the specified stream.
              

</td>
</tr>
</table>
 




## -remarks




        If the transform has a fixed number of input streams, the method returns <b>E_NOTIMPL</b>.
      


        An MFT might support this method but not allow certain input streams to be removed. If an input stream can be removed, the <a href="https://msdn.microsoft.com/d57ffac7-1a92-4c6b-bd59-0acd7239c0a6">IMFTransform::GetInputStreamInfo</a> method returns the <b>MFT_INPUT_STREAM_REMOVABLE</b> flag for that stream. Otherwise, the stream cannot be removed, and the method returns <b>MF_E_INVALIDREQUEST</b>. The method also fails if the MFT currently has the minimum number of input streams that it requires. To find the minimum number of streams, call <a href="https://msdn.microsoft.com/4d9585f0-5818-4e7f-925c-4c50ae6a6edc">IMFTransform::GetStreamLimits</a>.
      


        If the transform still has unprocessed input for that stream, the method might succeed or it might return <b>MF_E_TRANSFORM_INPUT_REMAINING</b>. If the method succeeds, the MFT will continue to process the remaining input after the stream is removed. If the method returns <b>MF_E_TRANSFORM_INPUT_REMAINING</b>, you must clear the input buffers before removing the stream. To clear the input buffers, either call <a href="https://msdn.microsoft.com/dc58cc75-7e01-4f47-a572-8e3ca1bc43b4">IMFTransform::ProcessOutput</a> or else call <a href="https://msdn.microsoft.com/a6dc67e5-8473-444a-8463-24f411e59565">IMFTransform::ProcessMessage</a> with the <b>MFT_MESSAGE_COMMAND_FLUSH</b> to flush the MFT. Then call the <b>DeleteInputStream</b> again. An MFT should never discard input buffers when <b>DeleteInputStream</b> is called.
      

If <b>MFT_UNIQUE_METHOD_NAMES</b> is defined before including mftransform.h, this method is renamed <b>MFTDeleteInputStream</b>. See <a href="comparison_of_mfts_and_dmos.htm">Creating Hybrid DMO/MFT Objects</a>.




## -see-also




<a href="https://msdn.microsoft.com/3cc502d8-d364-43b9-b0b6-d9474c002b20">IMFTransform</a>



<a href="https://msdn.microsoft.com/cb23fe0a-c42c-4912-a0bf-1f0b18a6f4e0">Media Foundation Transforms</a>
 

 

