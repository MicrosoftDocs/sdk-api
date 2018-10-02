---
UID: NF:mftransform.IMFTransform.SetOutputType
title: IMFTransform::SetOutputType
author: windows-sdk-content
description: Sets, tests, or clears the media type for an output stream on this Media Foundation transform (MFT).
old-location: mf\imftransform_setoutputtype.htm
tech.root: MedFound
ms.assetid: a9a1d03f-2e56-490c-885b-78c69dea8e92
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IMFTransform interface [Media Foundation],SetOutputType method, IMFTransform.SetOutputType, IMFTransform::SetOutputType, SetOutputType, SetOutputType method [Media Foundation], SetOutputType method [Media Foundation],IMFTransform interface, a9a1d03f-2e56-490c-885b-78c69dea8e92, mf.imftransform_setoutputtype, mftransform/IMFTransform::SetOutputType
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mftransform.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFTransform.SetOutputType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFTransform::SetOutputType


## -description


Sets, tests, or clears the media type for an output stream on this Media Foundation transform (MFT).
        


## -parameters




### -param dwOutputStreamID [in]

Output stream identifier. To get the list of stream identifiers, call <a href="https://msdn.microsoft.com/0715c78e-de92-439d-a4f3-078e19f78a8e">IMFTransform::GetStreamIDs</a>.
          


### -param pType [in]

Pointer to the <a href="https://msdn.microsoft.com/f1d60bec-71e4-4fcc-a020-92754b6f3c02">IMFMediaType</a> interface, or <b>NULL</b>.
          


### -param dwFlags [in]

Zero or more flags from the <a href="https://msdn.microsoft.com/dd7e97fb-80ab-4e6b-ac2a-a257d7e8ec63">_MFT_SET_TYPE_FLAGS</a> enumeration.
          


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
<dt><b>MF_E_INVALIDMEDIATYPE</b></dt>
</dl>
</td>
<td width="60%">
The transform cannot use the proposed media type.
              

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
<dt><b>MF_E_INVALIDTYPE</b></dt>
</dl>
</td>
<td width="60%">
The proposed type is not valid. This error code indicates that the media type itself is not configured correctly; for example, it might contain mutually contradictory flags.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_TRANSFORM_CANNOT_CHANGE_MEDIATYPE_WHILE_PROCESSING</b></dt>
</dl>
</td>
<td width="60%">
The MFT cannot switch types while processing data. Try draining or flushing the MFT.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_TRANSFORM_TYPE_NOT_SET</b></dt>
</dl>
</td>
<td width="60%">
You must set the input types before setting the output types.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_UNSUPPORTED_D3D_TYPE</b></dt>
</dl>
</td>
<td width="60%">
The MFT could not find a suitable DirectX Video Acceleration (DXVA) configuration.
              

</td>
</tr>
</table>
 




## -remarks



This method can be used to set, test without setting, or clear the media type:

<ul>
<li>To set the media type, set <i>dwFlags</i> to zero and set <i>pType</i> to a non-<b>NULL</b> pointer that specifies the media type.
          </li>
<li>To test the media type without setting it, set <i>dwFlags</i> to <b>MFT_SET_TYPE_TEST_ONLY</b> and set <i>pType</i> to a non-<b>NULL</b> pointer that specifies the media type. If the media type is acceptable, the method return <b>S_OK</b>. Otherwise, it returns <b>MF_E_INVALIDMEDIATYPE</b>. Regardless of the return value, the current media type does not change.
          </li>
<li>To clear the media type, set <i>pType</i> to <b>NULL</b>.
          </li>
</ul>
Setting the media type on one stream may change the acceptable types on another stream.
      

An MFT may require the caller to set one or more input types before setting the output type. If so, the method returns <b>MF_E_TRANSFORM_TYPE_NOT_SET</b>.
      

If the MFT supports DirectX Video Acceleration (DXVA) but is unable to find a suitable DXVA configuration (for example, if the graphics driver does not have the right capabilities), the method should return <b>MF_E_UNSUPPORTED_D3D_TYPE</b>. For more information, see <a href="https://msdn.microsoft.com/d7330370-adb3-4c6a-962a-7b46c344500c">Supporting DXVA 2.0 in Media Foundation</a>.

If <b>MFT_UNIQUE_METHOD_NAMES</b> is defined before including mftransform.h, this method is renamed <b>MFTSetOutputType</b>. See <a href="comparison_of_mfts_and_dmos.htm">Creating Hybrid DMO/MFT Objects</a>.




## -see-also




<a href="https://msdn.microsoft.com/3cc502d8-d364-43b9-b0b6-d9474c002b20">IMFTransform</a>



<a href="https://msdn.microsoft.com/cb23fe0a-c42c-4912-a0bf-1f0b18a6f4e0">Media Foundation Transforms</a>
 

 

