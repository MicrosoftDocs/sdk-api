---
UID: NF:mftransform.IMFTransform.GetInputStreamInfo
title: IMFTransform::GetInputStreamInfo
author: windows-sdk-content
description: Gets the buffer requirements and other information for an input stream on this Media Foundation transform (MFT).
old-location: mf\imftransform_getinputstreaminfo.htm
old-project: medfound
ms.assetid: d57ffac7-1a92-4c6b-bd59-0acd7239c0a6
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: GetInputStreamInfo, GetInputStreamInfo method [Media Foundation], GetInputStreamInfo method [Media Foundation],IMFTransform interface, IMFTransform interface [Media Foundation],GetInputStreamInfo method, IMFTransform.GetInputStreamInfo, IMFTransform::GetInputStreamInfo, d57ffac7-1a92-4c6b-bd59-0acd7239c0a6, mf.imftransform_getinputstreaminfo, mftransform/IMFTransform::GetInputStreamInfo
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
-	IMFTransform.GetInputStreamInfo
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFTransform::GetInputStreamInfo


## -description



          Gets the buffer requirements and other information for an input stream on this Media Foundation transform (MFT).
        


## -parameters




### -param dwInputStreamID [in]


            Input stream identifier. To get the list of stream identifiers, call <a href="https://msdn.microsoft.com/0715c78e-de92-439d-a4f3-078e19f78a8e">IMFTransform::GetStreamIDs</a>.
          


### -param pStreamInfo [out]


            Pointer to an <a href="https://msdn.microsoft.com/de3d6d70-3525-42a0-bc1a-2625e7ebd918">MFT_INPUT_STREAM_INFO</a> structure. The method fills the structure with information about the input stream.
          


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
<dt><b>MF_E_INVALIDSTREAMNUMBER</b></dt>
</dl>
</td>
<td width="60%">

                Invalid stream identifier.
              

</td>
</tr>
</table>
 




## -remarks



It is valid to call this method before setting the media types.

If <b>MFT_UNIQUE_METHOD_NAMES</b> is defined before including mftransform.h, this method is renamed <b>MFTGetInputStreamInfo</b>. See <a href="comparison_of_mfts_and_dmos.htm">Creating Hybrid DMO/MFT Objects</a>.




## -see-also




<a href="https://msdn.microsoft.com/3cc502d8-d364-43b9-b0b6-d9474c002b20">IMFTransform</a>



<a href="https://msdn.microsoft.com/cb23fe0a-c42c-4912-a0bf-1f0b18a6f4e0">Media Foundation Transforms</a>
 

 

