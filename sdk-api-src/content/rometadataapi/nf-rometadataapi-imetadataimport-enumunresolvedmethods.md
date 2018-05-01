---
UID: NF:rometadataapi.IMetaDataImport.EnumUnresolvedMethods
title: IMetaDataImport::EnumUnresolvedMethods method
author: windows-driver-content
description: Enumerates MemberDef tokens representing the unresolved methods in the current metadata scope.
old-location: winrt\imetadataimport_enumunresolvedmethods.htm
old-project: WinRT
ms.assetid: 8c10a1af-93a5-44d0-818f-f307f5f81075
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: EnumUnresolvedMethods method [Windows Runtime], EnumUnresolvedMethods method [Windows Runtime], IMetaDataImport interface, EnumUnresolvedMethods,IMetaDataImport.EnumUnresolvedMethods, IMetaDataImport, IMetaDataImport interface [Windows Runtime], EnumUnresolvedMethods method, IMetaDataImport::EnumUnresolvedMethods, rometadataapi/IMetaDataImport::EnumUnresolvedMethods, winrt.imetadataimport_enumunresolvedmethods
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
-	IMetaDataImport.EnumUnresolvedMethods
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IMetaDataImport::EnumUnresolvedMethods method


## -description


Enumerates MemberDef tokens representing the unresolved methods in the current metadata scope.


## -parameters




### -param phEnum [in, out]

A pointer to the enumerator. This must be NULL for the first call of this method.


### -param rgMethods [out]

The array used to store the MemberDef tokens.


### -param cMax [in]

The maximum size of the <i>rgMethods</i> array.


### -param pcTokens [out]

The number of MemberDef tokens returned in <i>rgMethods</i>.


## -returns



<table>
<tr>
<th>HRESULT</th>
<th>Description</th>
</tr>
<tr>
<td><b>S_OK</b></td>
<td><b>EnumUnresolvedMethods</b> returned successfully.</td>
</tr>
<tr>
<td><b>S_FALSE</b></td>
<td>There are no tokens to enumerate. In this case, <i>pcTokens</i> is 0 (zero).
 

</td>
</tr>
</table>
 




## -remarks



An unresolved method is one that has been declared but not implemented. A method is included in the enumeration if the method is marked <b>miForwardRef</b> and either <b>mdPinvokeImpl</b> or <b>miRuntime</b> is set to zero. In other words, an unresolved method is a class method that is marked <b>miForwardRef</b> but which is not implemented in unmanaged code (reached via PInvoke) nor implemented internally by the runtime itself. 



The enumeration excludes all methods that are defined either at module scope (globals) or in interfaces or abstract classes.




## -see-also




<a href="https://msdn.microsoft.com/5457d9d3-9a43-4e89-a52f-1254662ed92a">IMetaDataImport</a>
 

 

