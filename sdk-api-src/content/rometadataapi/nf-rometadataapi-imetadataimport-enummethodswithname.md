---
UID: NF:rometadataapi.IMetaDataImport.EnumMethodsWithName
title: IMetaDataImport::EnumMethodsWithName
author: windows-driver-content
description: Enumerates methods that have the specified name and that are defined by the type referenced by the specified TypeDef token.
old-location: winrt\imetadataimport_enummethodswithname.htm
old-project: WinRT
ms.assetid: 5252b535-23e5-4af1-91df-006717c4e159
ms.author: windowsdriverdev
ms.date: 5/15/2018
ms.keywords: EnumMethodsWithName, EnumMethodsWithName method [Windows Runtime], EnumMethodsWithName method [Windows Runtime],IMetaDataImport interface, IMetaDataImport interface [Windows Runtime],EnumMethodsWithName method, IMetaDataImport.EnumMethodsWithName, IMetaDataImport::EnumMethodsWithName, rometadataapi/IMetaDataImport::EnumMethodsWithName, winrt.imetadataimport_enummethodswithname
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
-	IMetaDataImport.EnumMethodsWithName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IMetaDataImport::EnumMethodsWithName


## -description


Enumerates methods that have the specified name and that are defined by the type referenced by the specified TypeDef token.


## -parameters




### -param phEnum [in, out]

A pointer to the enumerator. This must be NULL for the first call of this method.


### -param tkTypeDef [in]

A TypeDef token representing the type whose methods to enumerate.


### -param szName [in]

The name that limits the scope of the enumeration.


### -param rgMethods [out]

The array used to store the MethodDef tokens.


### -param cMax [in]

The maximum size of the <i>rgMethods</i> array.


### -param pcTokens [out]

The number of MethodDef tokens returned in <i>rgMethods</i>.


## -returns



<table>
<tr>
<th>HRESULT</th>
<th>Description</th>
</tr>
<tr>
<td><b>S_OK</b></td>
<td><b>EnumMethodsWithName</b> returned successfully.</td>
</tr>
<tr>
<td><b>S_FALSE</b></td>
<td>There are no tokens to enumerate. In this case, <i>pcTokens</i> is 0 (zero).
 

</td>
</tr>
</table>
 




## -remarks



This method enumerates fields and methods, but not properties or events. Unlike <a href="https://msdn.microsoft.com/3b0424d8-a0e3-4241-b957-d944e018cb31">EnumMethods</a>, <b>EnumMethodsWithName</b> discards all method tokens that do not have the specified name.




## -see-also




<a href="https://msdn.microsoft.com/5457d9d3-9a43-4e89-a52f-1254662ed92a">IMetaDataImport</a>
 

 

