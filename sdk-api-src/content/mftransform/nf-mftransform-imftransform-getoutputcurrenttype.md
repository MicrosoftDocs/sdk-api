---
UID: NF:mftransform.IMFTransform.GetOutputCurrentType
title: IMFTransform::GetOutputCurrentType
author: windows-driver-content
description: Gets the current media type for an output stream on this Media Foundation transform (MFT).
old-location: mf\imftransform_getoutputcurrenttype.htm
old-project: medfound
ms.assetid: 433c1918-4b87-40b1-a32b-db5cdd74d769
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: 433c1918-4b87-40b1-a32b-db5cdd74d769, GetOutputCurrentType, GetOutputCurrentType method [Media Foundation], GetOutputCurrentType method [Media Foundation],IMFTransform interface, IMFTransform interface [Media Foundation],GetOutputCurrentType method, IMFTransform.GetOutputCurrentType, IMFTransform::GetOutputCurrentType, mf.imftransform_getoutputcurrenttype, mftransform/IMFTransform::GetOutputCurrentType
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	IMFTransform.GetOutputCurrentType
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFTransform::GetOutputCurrentType


## -description



          Gets the current media type for an output stream on this Media Foundation transform (MFT).
        


## -parameters




### -param dwOutputStreamID [in]


            Output stream identifier. To get the list of stream identifiers, call <a href="https://msdn.microsoft.com/0715c78e-de92-439d-a4f3-078e19f78a8e">IMFTransform::GetStreamIDs</a>.
          


### -param ppType [out]


            Receives a pointer to the <a href="https://msdn.microsoft.com/f1d60bec-71e4-4fcc-a020-92754b6f3c02">IMFMediaType</a> interface. The caller must release the interface.
          


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
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_TRANSFORM_TYPE_NOT_SET</b></dt>
</dl>
</td>
<td width="60%">

                The output media type has not been set.
              

</td>
</tr>
</table>
 




## -remarks




        If the specified output stream does not yet have a media type, the method returns <b>MF_E_TRANSFORM_TYPE_NOT_SET</b>. Most MFTs do not set any default media types when first created. Instead, the client must set the media type by calling <a href="https://msdn.microsoft.com/a9a1d03f-2e56-490c-885b-78c69dea8e92">IMFTransform::SetOutputType</a>.
      

If <b>MFT_UNIQUE_METHOD_NAMES</b> is defined before including mftransform.h, this method is renamed <b>MFTGetOutputCurrentType</b>. See <a href="comparison_of_mfts_and_dmos.htm">Creating Hybrid DMO/MFT Objects</a>.

<h3><a id="Implementation_Notes"></a><a id="implementation_notes"></a><a id="IMPLEMENTATION_NOTES"></a>Implementation Notes</h3>
The MFT should return a clone of the media  type, not a pointer to the original type. Otherwise, the caller might modify the type and alter the internal state of the MFT.




## -see-also




<a href="https://msdn.microsoft.com/3cc502d8-d364-43b9-b0b6-d9474c002b20">IMFTransform</a>



<a href="https://msdn.microsoft.com/cb23fe0a-c42c-4912-a0bf-1f0b18a6f4e0">Media Foundation Transforms</a>
 

 

