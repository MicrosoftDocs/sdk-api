---
UID: NF:mftransform.IMFTransform.GetInputStreamAttributes
title: IMFTransform::GetInputStreamAttributes
author: windows-driver-content
description: Gets the attribute store for an input stream on this Media Foundation transform (MFT).
old-location: mf\imftransform_getinputstreamattributes.htm
old-project: medfound
ms.assetid: 2698da30-6913-41a9-9d98-f124cf31e591
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: 2698da30-6913-41a9-9d98-f124cf31e591, GetInputStreamAttributes, GetInputStreamAttributes method [Media Foundation], GetInputStreamAttributes method [Media Foundation],IMFTransform interface, IMFTransform interface [Media Foundation],GetInputStreamAttributes method, IMFTransform.GetInputStreamAttributes, IMFTransform::GetInputStreamAttributes, mf.imftransform_getinputstreamattributes, mftransform/IMFTransform::GetInputStreamAttributes
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
-	IMFTransform.GetInputStreamAttributes
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFTransform::GetInputStreamAttributes


## -description



          Gets the attribute store for an input stream on this Media Foundation transform (MFT).
        


## -parameters




### -param dwInputStreamID [in]


            Input stream identifier. To get the list of stream identifiers, call <a href="https://msdn.microsoft.com/0715c78e-de92-439d-a4f3-078e19f78a8e">IMFTransform::GetStreamIDs</a>.
          


### -param pAttributes






#### - ppAttributes [out]


            Receives a pointer to the <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a> interface. The caller must release the interface.
          


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

                The MFT does not support input stream attributes.
              

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




        
        Implementation of this method is optional unless the MFT needs to support a particular set of attributes. 


        To get the attribute store for the entire MFT, call <a href="https://msdn.microsoft.com/cb3ba2bc-550c-43b4-a69c-b546f2b92acc">IMFTransform::GetAttributes</a>.
      




## -see-also




<a href="https://msdn.microsoft.com/3cc502d8-d364-43b9-b0b6-d9474c002b20">IMFTransform</a>



<a href="https://msdn.microsoft.com/cb23fe0a-c42c-4912-a0bf-1f0b18a6f4e0">Media Foundation Transforms</a>



<a href="https://msdn.microsoft.com/9beb1306-1378-499c-b9e1-c768a7b4c8bc">Transform Attributes</a>
 

 

