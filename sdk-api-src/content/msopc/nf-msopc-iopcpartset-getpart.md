---
UID: NF:msopc.IOpcPartSet.GetPart
title: IOpcPartSet::GetPart
author: windows-sdk-content
description: Gets a part object, which represents a specified part, in the set.
old-location: opc\iopcpartset_getpart.htm
old-project: OPC
ms.assetid: 3a44725b-23a0-4338-b618-c0ce4ecde204
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetPart, GetPart method [Open Packaging Conventions], GetPart method [Open Packaging Conventions],IOpcPartSet interface, IOpcPartSet interface [Open Packaging Conventions],GetPart method, IOpcPartSet.GetPart, IOpcPartSet::GetPart, msopc/IOpcPartSet::GetPart, opc.iopcpartset_getpart
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msopc.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: OPC_SIGNATURE_TIME_FORMAT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msopc.h
api_name:
 - IOpcPartSet.GetPart
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IOpcPartSet::GetPart


## -description


Gets a part object, which represents a specified part, in the set.


## -parameters




### -param name [in]

A pointer to the <a href="https://msdn.microsoft.com/81123212-7a32-4833-b81f-8454a544327d">IOpcPartUri</a> interface of the part URI object that represents the part name of a part.


### -param part [out, retval]

A pointer to the <a href="https://msdn.microsoft.com/e6a40f30-03d1-4c93-a5e0-563b4c6588b4">IOpcPart</a> of the part object that represents the part that has the specified part name.


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
<dt><b>OPC_E_NO_SUCH_PART</b></dt>
<dt>0x80510018</dt>
</dl>
</td>
<td width="60%">
The specified part does not exist.

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



To retrieve the <a href="https://msdn.microsoft.com/e6a40f30-03d1-4c93-a5e0-563b4c6588b4">IOpcPart</a> interface pointer of the part object that represents a specific part, call the <a href="https://msdn.microsoft.com/721e0252-330a-4218-9267-b3dd0dea7598">PartExists</a> method and pass in the part name to confirm that the part is represented in the set. If it is, call the <b>GetPart</b> method and pass in the part name to retrieve the <b>IOpcPart</b> interface pointer.

If the part URI object represents the part name of a Relationships part, this method will fail because Relationships parts are not included in the set.

The <a href="https://msdn.microsoft.com/e6a40f30-03d1-4c93-a5e0-563b4c6588b4">IOpcPart</a> interface provides access to the properties of a part. For details about these properties, see the <a href="https://msdn.microsoft.com/95da581d-3d30-4cd7-bd20-f44bf505ac0a">Parts Overview</a> and <a href="https://msdn.microsoft.com/e6a40f30-03d1-4c93-a5e0-563b4c6588b4">IOpcPart</a>.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>.




## -see-also




<a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>



<a href="https://msdn.microsoft.com/f34c682f-7677-4d20-bd37-b1a68293d85c">IOpcPartSet</a>



<b>Overviews</b>



<a href="https://msdn.microsoft.com/7ab1cc09-ce81-4f56-8adf-d8c95bf2c4cd">Packaging API Reference</a>



<a href="https://msdn.microsoft.com/885137be-35d5-4ec5-bbcc-16c95adf55ab">Packaging API Samples</a>



<a href="https://msdn.microsoft.com/b4cd8f69-3559-46a0-95ec-6fcaab21959c">Packaging Errors</a>



<a href="https://msdn.microsoft.com/95da581d-3d30-4cd7-bd20-f44bf505ac0a">Parts Overview</a>



<b>Reference</b>
 

 

