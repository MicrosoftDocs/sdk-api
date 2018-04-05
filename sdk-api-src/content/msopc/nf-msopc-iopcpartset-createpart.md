---
UID: NF:msopc.IOpcPartSet.CreatePart
title: IOpcPartSet::CreatePart method
author: windows-driver-content
description: Creates a part object that represents a part and adds a pointer to the object's IOpcPart interface to the set.
old-location: opc\iopcpartset_createpart.htm
old-project: OPC
ms.assetid: 8c5de7ac-f51c-42f2-9068-8e9ede86ad97
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: CreatePart method [Open Packaging Conventions], CreatePart method [Open Packaging Conventions], IOpcPartSet interface, CreatePart,IOpcPartSet.CreatePart, IOpcPartSet, IOpcPartSet interface [Open Packaging Conventions], CreatePart method, IOpcPartSet::CreatePart, msopc/IOpcPartSet::CreatePart, opc.iopcpartset_createpart
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msopc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Opcobjectmodel.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: OPC_SIGNATURE_TIME_FORMAT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	msopc.h
api_name:
-	IOpcPartSet.CreatePart
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IOpcPartSet::CreatePart method


## -description


Creates a part object that represents a part and adds a pointer to the object's <a href="https://msdn.microsoft.com/e6a40f30-03d1-4c93-a5e0-563b4c6588b4">IOpcPart</a> interface to the set.


## -parameters




### -param name [in]

A pointer to the  <a href="https://msdn.microsoft.com/81123212-7a32-4833-b81f-8454a544327d">IOpcPartUri</a> interface of a part URI object that represents the part name of the part.

To create  a part URI object (which implements the <a href="https://msdn.microsoft.com/81123212-7a32-4833-b81f-8454a544327d">IOpcPartUri</a> interface) to represent the part name of the part, call the <a href="https://msdn.microsoft.com/8634d166-767a-46a5-9001-5fca88bfa844">IOpcFactory::CreatePartUri</a> method.


### -param contentType [in]

The media type of part content.


### -param compressionOptions [in]

A value that describes the way to compress the part content of the part.


### -param part [out, retval]

A pointer to the new <a href="https://msdn.microsoft.com/e6a40f30-03d1-4c93-a5e0-563b4c6588b4">IOpcPart</a> that represents the part.

This parameter cannot be <b>NULL</b>.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code/value</th>
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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>name</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The value passed in the <i>compressionOptions</i> parameter is not a valid <a href="https://msdn.microsoft.com/bc821e84-fd18-449c-89d0-a261f43f8971">OPC_COMPRESSION_OPTIONS</a> enumeration value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_DUPLICATE_PART</b></dt>
<dt>0x8051000B</dt>
</dl>
</td>
<td width="60%">
A part with the specified part name already exists in the current package.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_INVALID_CONTENT_TYPE</b></dt>
<dt>0x80510044</dt>
</dl>
</td>
<td width="60%">
A content type does not conform to the rules for a valid media type, specified in <a href="http://go.microsoft.com/fwlink/p/?linkid=143979">RFC 2616: HTTP/1.1</a> (http://go.microsoft.com/fwlink/p/?linkid=143979) and the <i>OPC</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_UNEXPECTED_CONTENT_TYPE</b></dt>
<dt>0x80510005</dt>
</dl>
</td>
<td width="60%">
Either the content type of a part differed from the expected content type (specified in the OPC, <a href="http://go.microsoft.com/fwlink/p/?linkid=123375">ECMA-376 Part 2</a>), or the part content did not match the part's  content type.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Package Consumption error</b></dt>
</dl>
</td>
<td width="60%">

          An <b>HRESULT</b> error code from the <a href="https://msdn.microsoft.com/0ad335ff-57da-4d4a-95c0-6b9b513a9698">Package Consumption Error Group</a>.
        

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Part URI error</b></dt>
</dl>
</td>
<td width="60%">

          An <b>HRESULT</b> error code from the <a href="https://msdn.microsoft.com/877447bb-d4e1-4277-b8ce-cb7a31a33fe0">Part URI Error Group</a>.
        

</td>
</tr>
</table>
 




## -remarks



When a part object is created and a pointer to it is added to the set, the part it represents is serialized when the package is serialized.

This method cannot create a part object that represents a Relationships part.

If part content is compressed prior to the creation of the part object, pass the <b>OPC_COMPRESSION_NONE</b> value in the <i>compressionOptions</i> parameter.

Part content that is already compressed will not compress significantly more.

An <a href="https://msdn.microsoft.com/e6a40f30-03d1-4c93-a5e0-563b4c6588b4">IOpcPart</a> provides access to the properties of a part. For details about these properties, see the <a href="https://msdn.microsoft.com/95da581d-3d30-4cd7-bd20-f44bf505ac0a">Parts Overview</a> and the <a href="https://msdn.microsoft.com/e6a40f30-03d1-4c93-a5e0-563b4c6588b4">IOpcPart</a> topic.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>.




## -see-also




<a href="http://go.microsoft.com/fwlink/p/?linkid=123375">ECMA-376 OpenXML</a>



<b>External Resources</b>



<a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>



<a href="https://msdn.microsoft.com/8634d166-767a-46a5-9001-5fca88bfa844">IOpcFactory::CreatePartUri</a>



<a href="https://msdn.microsoft.com/f34c682f-7677-4d20-bd37-b1a68293d85c">IOpcPartSet</a>



<a href="https://msdn.microsoft.com/bc821e84-fd18-449c-89d0-a261f43f8971">OPC_COMPRESSION_OPTIONS</a>



<b>Overviews</b>



<a href="https://msdn.microsoft.com/7ab1cc09-ce81-4f56-8adf-d8c95bf2c4cd">Packaging API Reference</a>



<a href="https://msdn.microsoft.com/885137be-35d5-4ec5-bbcc-16c95adf55ab">Packaging API Samples</a>



<a href="https://msdn.microsoft.com/b4cd8f69-3559-46a0-95ec-6fcaab21959c">Packaging Errors</a>



<a href="https://msdn.microsoft.com/95da581d-3d30-4cd7-bd20-f44bf505ac0a">Parts Overview</a>



<a href="http://go.microsoft.com/fwlink/p/?linkid=143979">RFC 2616: HTTP/1.1</a>



<b>Reference</b>
 

 

