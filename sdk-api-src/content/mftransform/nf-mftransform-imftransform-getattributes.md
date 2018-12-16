---
UID: NF:mftransform.IMFTransform.GetAttributes
title: IMFTransform::GetAttributes
author: windows-sdk-content
description: Gets the global attribute store for this Media Foundation transform (MFT).
old-location: mf\imftransform_getattributes.htm
tech.root: medfound
ms.assetid: cb3ba2bc-550c-43b4-a69c-b546f2b92acc
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetAttributes, GetAttributes method [Media Foundation], GetAttributes method [Media Foundation],IMFTransform interface, IMFTransform interface [Media Foundation],GetAttributes method, IMFTransform.GetAttributes, IMFTransform::GetAttributes, cb3ba2bc-550c-43b4-a69c-b546f2b92acc, mf.imftransform_getattributes, mftransform/IMFTransform::GetAttributes
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
 - IMFTransform.GetAttributes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFTransform::GetAttributes


## -description


Gets the global attribute store for this Media Foundation transform (MFT).
        


## -parameters




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
The MFT does not support attributes.
              

</td>
</tr>
</table>
 




## -remarks



Use the <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a> pointer retrieved by this method to get or set attributes that apply to the entire MFT. To get the attribute store for an input stream, call <a href="https://msdn.microsoft.com/2698da30-6913-41a9-9d98-f124cf31e591">IMFTransform::GetInputStreamAttributes</a>. To get the attribute store for an output stream, call <a href="https://msdn.microsoft.com/d54ce20c-8ef9-4480-9ddd-908751fc0a7e">IMFTransform::GetOutputStreamAttributes</a>.
      

Implementation of this method is optional unless the MFT needs to support a particular set of attributes. Exception: Hardware-based MFTs must implement this method. See <a href="https://msdn.microsoft.com/9922d403-5d0d-433f-ad9f-c86142ac0f46">Hardware MFTs</a>.




## -see-also




<a href="https://msdn.microsoft.com/3cc502d8-d364-43b9-b0b6-d9474c002b20">IMFTransform</a>



<a href="https://msdn.microsoft.com/cb23fe0a-c42c-4912-a0bf-1f0b18a6f4e0">Media Foundation Transforms</a>



<a href="https://msdn.microsoft.com/9beb1306-1378-499c-b9e1-c768a7b4c8bc">Transform Attributes</a>
 

 

