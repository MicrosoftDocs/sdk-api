---
UID: NF:mfobjects.MFSerializeAttributesToStream
title: MFSerializeAttributesToStream function
author: windows-sdk-content
description: Writes the contents of an attribute store to a stream.
old-location: mf\mfserializeattributestostream.htm
tech.root: medfound
ms.assetid: b8bc88e5-19ae-46b3-aa78-a00afee1f481
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: MFSerializeAttributesToStream, MFSerializeAttributesToStream function [Media Foundation], b8bc88e5-19ae-46b3-aa78-a00afee1f481, mf.mfserializeattributestostream, mfobjects/MFSerializeAttributesToStream
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mfobjects.h
req.include-header: Mfidl.h
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
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFSerializeAttributesToStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MFSerializeAttributesToStream function


## -description



Writes the contents of an attribute store to a stream.




## -parameters




### -param pAttr

Pointer to the <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a> interface of the attribute store.


### -param dwOptions

Bitwise <b>OR</b> of zero or more flags from the <a href="https://msdn.microsoft.com/e4b218d1-185c-483f-b697-19ce8b3a4058">MF_ATTRIBUTE_SERIALIZE_OPTIONS</a> enumeration.


### -param pStm

Pointer to the <b>IStream</b> interface of the stream where the attributes are saved.


## -returns



The function returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
</table>
 




## -remarks



If <i>dwOptions</i> contains the MF_ATTRIBUTE_SERIALIZE_UNKNOWN_BYREF flag, the function serializes <b>IUnknown</b> pointers in the attribute store, as follows:

<ul>
<li>
If the <b>IStream</b> pointer exposes the <a href="https://msdn.microsoft.com/9d29befd-b0ae-4610-a0b7-17face03c45e">IMFObjectReferenceStream</a> interface (through <b>QueryInterface</b>), the function calls <a href="https://msdn.microsoft.com/776f94c4-d0e9-4fb7-a39c-32c83428bbe3">IMFObjectReferenceStream::SaveReference</a> to serialize each pointer.

</li>
<li>
Otherwise, the function calls <b>CoMarshalInterface</b> to serialize a proxy for the object.

</li>
</ul>
If <i>dwOptions</i> does not include the MF_ATTRIBUTE_SERIALIZE_UNKNOWN_BYREF flag, the function skips <b>IUnknown</b> pointers in the attribute store.

To load the attributes from the stream, call <a href="https://msdn.microsoft.com/cc0bccfd-7e67-4e55-9d3e-ebcd91b94a3a">MFDeserializeAttributesFromStream</a>.

The main purpose of this function is to marshal attributes across process boundaries.




## -see-also




<a href="https://msdn.microsoft.com/44af5e03-5f0a-4564-b9d6-b8c935df35b2">Attributes and Properties</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

