---
UID: NF:rometadataapi.IMetaDataImport.EnumMembers
title: IMetaDataImport::EnumMembers
author: windows-sdk-content
description: Enumerates MemberDef tokens representing members of the specified type.
old-location: winrt\imetadataimport_enummembers.htm
old-project: WinRT
ms.assetid: cb1e90fe-e5c8-4f6d-b38a-ae7f46cb34e9
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: EnumMembers, EnumMembers method [Windows Runtime], EnumMembers method [Windows Runtime],IMetaDataImport interface, IMetaDataImport interface [Windows Runtime],EnumMembers method, IMetaDataImport.EnumMembers, IMetaDataImport::EnumMembers, rometadataapi/IMetaDataImport::EnumMembers, winrt.imetadataimport_enummembers
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: rometadataapi.h
req.include-header: 
req.redist: 
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
 - IMetaDataImport.EnumMembers
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IMetaDataImport::EnumMembers


## -description


Enumerates MemberDef tokens representing members of the specified type.


## -parameters




### -param phEnum [in, out]

A pointer to the enumerator.


### -param tkTypeDef [in]

A TypeDef token representing the type whose members are to be enumerated.


### -param rgMembers [out]

The array used to hold the MemberDef tokens.


### -param cMax [in]

The maximum size of the <i>rgMembers</i> array.


### -param pcTokens [out]

The actual number of MemberDef tokens returned in <i>rgMembers</i>.


## -returns



<table>
<tr>
<th>HRESULT</th>
<th>Description</th>
</tr>
<tr>
<td><b>S_OK</b></td>
<td><b>EnumMembers</b> returned successfully.</td>
</tr>
<tr>
<td><b>S_FALSE</b></td>
<td>There are no MemberRef tokens to enumerate. In this case, <i>pcTokens</i> is 0 (zero).
 

</td>
</tr>
</table>
 




## -remarks



When enumerating collections of members for a class, <b>EnumMembers</b> returns only members defined directly on the class. It does not return any members that the class inherits, even if the class provides an implementation for those inherited members. To enumerate inherited members, the caller must explicitly walk the inheritance chain. Note that the rules for the inheritance chain may vary depending on the language or compiler that emitted the original metadata.






## -see-also




<a href="https://msdn.microsoft.com/5457d9d3-9a43-4e89-a52f-1254662ed92a">IMetaDataImport</a>
 

 

