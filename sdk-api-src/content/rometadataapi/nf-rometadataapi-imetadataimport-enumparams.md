---
UID: NF:rometadataapi.IMetaDataImport.EnumParams
title: IMetaDataImport::EnumParams
author: windows-driver-content
description: Enumerates ParamDef tokens representing the parameters of the method referenced by the specified MethodDef token.
old-location: winrt\imetadataimport_enumparams.htm
old-project: WinRT
ms.assetid: 0d3cc66e-575d-4451-bab7-e3dd24fd5060
ms.author: windowsdriverdev
ms.date: 5/15/2018
ms.keywords: EnumParams, EnumParams method [Windows Runtime], EnumParams method [Windows Runtime],IMetaDataImport interface, IMetaDataImport interface [Windows Runtime],EnumParams method, IMetaDataImport.EnumParams, IMetaDataImport::EnumParams, rometadataapi/IMetaDataImport::EnumParams, winrt.imetadataimport_enumparams
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: RO_ERROR_REPORTING_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	rometadataapi.h
api_name:
-	IMetaDataImport.EnumParams
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IMetaDataImport::EnumParams


## -description


Enumerates ParamDef tokens representing the parameters of the method referenced by the specified MethodDef token.


## -parameters




### -param phEnum [in, out]

 A pointer to the enumerator. This must be NULL for the first call of this method.


### -param tkMethodDef [in]

A MethodDef token representing the method with the parameters to enumerate.


### -param rParams [out]

The array used to store the ParamDef tokens.


### -param cMax [in]

The maximum size of the <i>rParams array</i>.


### -param pcTokens [out]

The number of ParamDef tokens returned in <i>rParams</i>.


## -returns



<table>
<tr>
<th>HRESULT</th>
<th>Description</th>
</tr>
<tr>
<td><b>S_OK</b></td>
<td><b>EnumParams</b> returned successfully.</td>
</tr>
<tr>
<td><b>S_FALSE</b></td>
<td>There are no tokens to enumerate. In this case, <i>pcTokens</i> is 0 (zero).
 

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/5457d9d3-9a43-4e89-a52f-1254662ed92a">IMetaDataImport</a>
 

 

