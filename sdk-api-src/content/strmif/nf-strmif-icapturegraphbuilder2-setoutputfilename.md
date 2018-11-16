---
UID: NF:strmif.ICaptureGraphBuilder2.SetOutputFileName
title: ICaptureGraphBuilder2::SetOutputFileName
author: windows-sdk-content
description: The SetOutputFileName method creates the file writing section of the filter graph.
old-location: dshow\icapturegraphbuilder2_setoutputfilename.htm
tech.root: DirectShow
ms.assetid: b81a79c1-a6f2-4c80-ae86-095fb9f78673
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ICaptureGraphBuilder2 interface [DirectShow],SetOutputFileName method, ICaptureGraphBuilder2.SetOutputFileName, ICaptureGraphBuilder2::SetOutputFileName, ICaptureGraphBuilder2SetOutputFileName, SetOutputFileName, SetOutputFileName method [DirectShow], SetOutputFileName method [DirectShow],ICaptureGraphBuilder2 interface, dshow.icapturegraphbuilder2_setoutputfilename, strmif/ICaptureGraphBuilder2::SetOutputFileName
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - ICaptureGraphBuilder2.SetOutputFileName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- strmif.h
: 
- ICaptureGraphBuilder2.SetOutputFileName
: 
---

# ICaptureGraphBuilder2::SetOutputFileName


## -description



The <code>SetOutputFileName</code> method creates the file writing section of the filter graph.




## -parameters




### -param pType [in]

Pointer to a <b>GUID</b> that represents either the media subtype of the output or the class identifier (CLSID) of a multiplexer filter or file writer filter. If you specify a media subtype, it must be one of the following:

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>MEDIASUBTYPE_Avi</td>
<td>Audio-Video Interleaved (AVI)</td>
</tr>
<tr>
<td>MEDIASUBTYPE_Asf</td>
<td>Advanced Systems Format (ASF)</td>
</tr>
</table>
 


### -param lpstrFile [in]

Pointer to a wide-character string that contains the output file name.


### -param ppf [out]

Address of a pointer that receives the multiplexer's <a href="https://msdn.microsoft.com/d8c09dc7-dae8-4b51-8da8-69e64928a091">IBaseFilter</a> interface.


### -param ppSink [out]

Address of a pointer that receives the file writer's <a href="https://msdn.microsoft.com/aa1d3f8e-9790-4442-ba7e-896981bf1b96">IFileSinkFilter</a> interface. Can be <b>NULL</b>.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Failure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
</table>
 




## -remarks



This method creates a multiplexer filter based on the value of the <i>pType</i> parameter. For AVI, it creates the <a href="https://msdn.microsoft.com/31d30c91-fc6a-45ec-a2e0-34e6a1e902a4">AVI Mux Filter</a>. For ASF, it creates the <a href="https://msdn.microsoft.com/1b12f65f-8d77-4d38-aad9-92bb15cc0426">WM ASF Writer</a>. For other values, it creates the filter identified by the CLSID. It adds the multiplexer to the filter graph, and returns a pointer to its <b>IBaseFilter</b> interface in the <i>ppf</i> parameter.

If the multiplexer supports the <b>IFileSinkFilter</b> interface, the method calls <a href="https://msdn.microsoft.com/d202be46-0a7a-4097-adf6-6ec9c6274449">IFileSinkFilter::SetFileName</a> to set the output file name, using the value given in the <i>lpwstrFile</i> parameter. If the multiplexer does not support <b>IFileSinkFilter</b> interface, the method adds the <a href="https://msdn.microsoft.com/2bfbea8a-679f-4656-9ff3-fdf34aa0eb26">File Writer Filter</a> to the filter graph, connects the multiplexer to the file writer, and uses the file writer's <b>IFileSinkFilter</b> interface to call <b>SetFileName</b>. If the <i>pSink</i> parameter is not <b>NULL</b>, it receives a pointer to the <b>IFileSinkFilter</b> interface.

You can use the pointer to the multiplexer filter, returned in the <i>ppf</i> parameter, as the <i>pSink</i> parameter in the <a href="https://msdn.microsoft.com/2fb5f13c-2bf5-463b-a209-77129a159bd6">ICaptureGraphBuilder2::RenderStream</a> method.

For custom multiplexer filters, the method fails if the filter does not support a connection on its output pin before its input pins are connected. For example, the <a href="https://msdn.microsoft.com/b7102e39-b3c7-42fb-a89b-f05f3ee75df7">WavDest Filter Sample</a> included with the SDK has this limitation.

If the method succeeds, the <b>IBaseFilter</b> interface returned in the <i>ppf</i> parameter has an outstanding reference count. If the method succeeds and <i>pSink</i> is not <b>NULL</b>, the <b>IFileSinkFilter</b> interface also has an outstanding reference count. Be sure to release both interfaces when you are done using them.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/abdf6fb2-e98f-4df8-98ec-06d33798abb5">ICaptureGraphBuilder2 Interface</a>
 

 

