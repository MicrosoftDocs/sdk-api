---
UID: NF:mfobjects.MFDeserializeAttributesFromStream
title: MFDeserializeAttributesFromStream function
author: windows-sdk-content
description: Loads attributes from a stream into an attribute store.
old-location: mf\mfdeserializeattributesfromstream.htm
tech.root: medfound
ms.assetid: cc0bccfd-7e67-4e55-9d3e-ebcd91b94a3a
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: MFDeserializeAttributesFromStream, MFDeserializeAttributesFromStream function [Media Foundation], cc0bccfd-7e67-4e55-9d3e-ebcd91b94a3a, mf.mfdeserializeattributesfromstream, mfobjects/MFDeserializeAttributesFromStream
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
 - MFDeserializeAttributesFromStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MFDeserializeAttributesFromStream function


## -description



Loads attributes from a stream into an attribute store.




## -parameters




### -param pAttr

Pointer to the <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a> interface of the attribute store.


### -param dwOptions

Bitwise <b>OR</b> of zero or more flags from the <a href="https://msdn.microsoft.com/e4b218d1-185c-483f-b697-19ce8b3a4058">MF_ATTRIBUTE_SERIALIZE_OPTIONS</a> enumeration.


### -param pStm

Pointer to the <b>IStream</b> interface of the stream from which to read the attributes.


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



Use this function to deserialize an attribute store that was serialized with the <a href="https://msdn.microsoft.com/b8bc88e5-19ae-46b3-aa78-a00afee1f481">MFSerializeAttributesToStream</a> function.

If <i>dwOptions</i> contains the MF_ATTRIBUTE_SERIALIZE_UNKNOWN_BYREF flag, the function deserializes <b>IUnknown</b> pointers from the stream, as follows:

<ul>
<li>
If the <b>IStream</b> pointer exposes the <a href="https://msdn.microsoft.com/9d29befd-b0ae-4610-a0b7-17face03c45e">IMFObjectReferenceStream</a> interface (through <b>QueryInterface</b>), the function calls <a href="https://msdn.microsoft.com/fabf7de2-8433-43ba-9ded-001569614054">IMFObjectReferenceStream::LoadReference</a> to deserialize each pointer.

</li>
<li>
Otherwise, the function calls <b>CoUnmarshalInterface</b> to deserialize a proxy for the object.

</li>
</ul>
This function deletes any attributes that were previously stored in <i>pAttr</i>.




## -see-also




<a href="https://msdn.microsoft.com/44af5e03-5f0a-4564-b9d6-b8c935df35b2">Attributes and Properties</a>



<a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a>



<a href="https://msdn.microsoft.com/e4b218d1-185c-483f-b697-19ce8b3a4058">MF_ATTRIBUTE_SERIALIZE_OPTIONS</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

