---
UID: NF:rometadataapi.IMetaDataImport2.EnumMethodSpecs
title: IMetaDataImport2::EnumMethodSpecs
author: windows-sdk-content
description: Gets an enumerator for an array of MethodSpec tokens associated with the specified MethodDef or MemberRef token.
old-location: winrt\imetadataimport2_enummethodspecs.htm
old-project: WinRT
ms.assetid: b4327a57-8a19-44f9-90b6-df2b089f63e4
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: EnumMethodSpecs, EnumMethodSpecs method [Windows Runtime], EnumMethodSpecs method [Windows Runtime],IMetaDataImport2 interface, IMetaDataImport2 interface [Windows Runtime],EnumMethodSpecs method, IMetaDataImport2.EnumMethodSpecs, IMetaDataImport2::EnumMethodSpecs, rometadataapi/IMetaDataImport2::EnumMethodSpecs, winrt.imetadataimport2_enummethodspecs
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: RO_ERROR_REPORTING_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - rometadataapi.h
api_name:
 - IMetaDataImport2.EnumMethodSpecs
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IMetaDataImport2::EnumMethodSpecs


## -description


Gets an enumerator for an array of MethodSpec tokens associated with the specified MethodDef or MemberRef token.


## -parameters




### -param phEnum [in, out]

 pointer to the enumerator for <i>rMethodSpecs</i>.


### -param tk [in]

The <b>MemberRef</b> or <b>MethodDef</b> token that represents the method whose <b>MethodSpec</b> tokens are to be enumerated. If the value of <i>tk</i> is 0 (zero), all <b>MethodSpec</b> tokens in the scope will be enumerated.


### -param rMethodSpecs [out]

The array of <b>MethodSpec</b> tokens to enumerate.


### -param cMax [in]

The requested maximum number of tokens to place in <i>rMethodSpecs</i>.


### -param pcMethodSpecs [out]

The returned number of tokens placed in <i>rMethodSpecs</i>.


## -returns



<table>
<tr>
<th>HRESULT</th>
<th>Description</th>
</tr>
<tr>
<td><b>S_OK</b></td>
<td><b>EnumMethodSpecs</b> returned successfully.</td>
</tr>
<tr>
<td><b>S_FALSE</b></td>
<td><i>phEnum</i> has no member elements. In this case, <i>pcMethodSpecs</i> is set to 0 (zero).
 

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/32c462e0-d4b8-44db-b24b-c86b46be85bf">IMetaDataImport2</a>
 

 

