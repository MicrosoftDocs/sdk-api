---
UID: NN:rometadataapi.IMetaDataImport2
title: IMetaDataImport2 (rometadataapi.h)
author: windows-sdk-content
description: Extends the IMetaDataImport interface to provide the capability of working with generic types.
old-location: winrt\imetadataimport2.htm
tech.root: WinRT
ms.assetid: 32c462e0-d4b8-44db-b24b-c86b46be85bf
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMetaDataImport2, IMetaDataImport2 interface [Windows Runtime], IMetaDataImport2 interface [Windows Runtime],described, rometadataapi/IMetaDataImport2, winrt.imetadataimport2
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
ms.custom: 19H1
---

# IMetaDataImport2 interface


## -description


Extends the <a href="https://docs.microsoft.com/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadataimport">IMetaDataImport</a> interface to provide the capability of working with generic types.


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
<a href="https://docs.microsoft.com/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataimport2-enumgenericparamconstraints">EnumGenericParamConstraints</a>
</td>
<td align="left" width="63%">
Gets an enumerator for an array of generic parameter constraints associated with the generic parameter represented by the specified token.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataimport2-enumgenericparams">EnumGenericParams</a>
</td>
<td align="left" width="63%">
Gets an enumerator for an array of generic parameter tokens associated with the specified TypeDef or MethodDef token.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataimport2-enummethodspecs">EnumMethodSpecs</a>
</td>
<td align="left" width="63%">
Gets an enumerator for an array of MethodSpec tokens associated with the specified MethodDef or MemberRef token.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataimport2-getgenericparamconstraintprops">GetGenericParamConstraintProps</a>
</td>
<td align="left" width="63%">
Gets the metadata associated with the generic parameter constraint represented by the specified constraint token.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataimport2-getgenericparamprops">GetGenericParamProps</a>
</td>
<td align="left" width="63%">
Gets the metadata associated with the generic parameter represented by the specified token.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataimport2-getmethodspecprops">GetMethodSpecProps</a>
</td>
<td align="left" width="63%">
Gets the metadata signature of the method referenced by the specified MethodSpec token.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataimport2-getpekind">GetPEKind</a>
</td>
<td align="left" width="63%">
Gets a value identifying the nature of the code in the portable executable (PE) file, typically a DLL or EXE file, that is defined in the current metadata scope.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataimport2-getversionstring">GetVersionString</a>
</td>
<td align="left" width="63%">
Gets the version number of the runtime that was used to build the assembly.

</td>
</tr>
</table> 

