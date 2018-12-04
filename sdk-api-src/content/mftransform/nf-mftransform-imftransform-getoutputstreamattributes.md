---
UID: NF:mftransform.IMFTransform.GetOutputStreamAttributes
title: IMFTransform::GetOutputStreamAttributes
author: windows-sdk-content
description: Gets the attribute store for an output stream on this Media Foundation transform (MFT).
old-location: mf\imftransform_getoutputstreamattributes.htm
tech.root: medfound
ms.assetid: d54ce20c-8ef9-4480-9ddd-908751fc0a7e
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: GetOutputStreamAttributes, GetOutputStreamAttributes method [Media Foundation], GetOutputStreamAttributes method [Media Foundation],IMFTransform interface, IMFTransform interface [Media Foundation],GetOutputStreamAttributes method, IMFTransform.GetOutputStreamAttributes, IMFTransform::GetOutputStreamAttributes, d54ce20c-8ef9-4480-9ddd-908751fc0a7e, mf.imftransform_getoutputstreamattributes, mftransform/IMFTransform::GetOutputStreamAttributes
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
 - IMFTransform.GetOutputStreamAttributes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFTransform::GetOutputStreamAttributes


## -description


Gets the attribute store for an output stream on this Media Foundation transform (MFT).
        


## -parameters




### -param dwOutputStreamID [in]

Output stream identifier. To get the list of stream identifiers, call <a href="https://msdn.microsoft.com/0715c78e-de92-439d-a4f3-078e19f78a8e">IMFTransform::GetStreamIDs</a>.
          


### -param pAttributes [out]

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
The MFT does not support output stream attributes.
              

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
 

 

