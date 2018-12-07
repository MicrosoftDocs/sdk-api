---
UID: NN:rometadataapi.IMetaDataImport2
title: IMetaDataImport2
author: windows-sdk-content
description: Extends the IMetaDataImport interface to provide the capability of working with generic types.
old-location: winrt\imetadataimport2.htm
tech.root: WinRT
ms.assetid: 32c462e0-d4b8-44db-b24b-c86b46be85bf
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMetaDataImport2, IMetaDataImport2 interface [Windows Runtime], IMetaDataImport2 interface [Windows Runtime],described, rometadataapi/IMetaDataImport2, winrt.imetadataimport2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: rometadataapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Rometadataapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - rometadataapi.h
api_name:
 - IMetaDataImport2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMetaDataImport2 interface


## -description


Extends the <a href="https://msdn.microsoft.com/5457d9d3-9a43-4e89-a52f-1254662ed92a">IMetaDataImport</a> interface to provide the capability of working with generic types.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMetaDataImport2</b> interface inherits from <b>IMetaDataImport</b>. <b>IMetaDataImport2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMetaDataImport2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5e8ba48d-7c94-4fc6-8def-db296065fdce">EnumGenericParamConstraints</a>
</td>
<td align="left" width="63%">
Gets an enumerator for an array of generic parameter constraints associated with the generic parameter represented by the specified token.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7ad0d834-7b77-4c90-b28f-fc9e54e9deb7">EnumGenericParams</a>
</td>
<td align="left" width="63%">
Gets an enumerator for an array of generic parameter tokens associated with the specified TypeDef or MethodDef token.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b4327a57-8a19-44f9-90b6-df2b089f63e4">EnumMethodSpecs</a>
</td>
<td align="left" width="63%">
Gets an enumerator for an array of MethodSpec tokens associated with the specified MethodDef or MemberRef token.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/307b4ab5-733d-4340-a400-3a13039099b0">GetGenericParamConstraintProps</a>
</td>
<td align="left" width="63%">
Gets the metadata associated with the generic parameter constraint represented by the specified constraint token.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3967e82c-64e3-4d05-b10a-e4e86f9f60ab">GetGenericParamProps</a>
</td>
<td align="left" width="63%">
Gets the metadata associated with the generic parameter represented by the specified token.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/498ee212-000d-4204-ae7a-de553bf3ea45">GetMethodSpecProps</a>
</td>
<td align="left" width="63%">
Gets the metadata signature of the method referenced by the specified MethodSpec token.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ece40ffa-f92f-4f27-b03c-75204e0c6ee1">GetPEKind</a>
</td>
<td align="left" width="63%">
Gets a value identifying the nature of the code in the portable executable (PE) file, typically a DLL or EXE file, that is defined in the current metadata scope.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9f04ee6f-4a7d-4cdb-868e-eec2e9f41678">GetVersionString</a>
</td>
<td align="left" width="63%">
Gets the version number of the runtime that was used to build the assembly.

</td>
</tr>
</table> 

