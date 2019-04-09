---
UID: NF:rometadataapi.IMetaDataImport.EnumPermissionSets
title: IMetaDataImport::EnumPermissionSets (rometadataapi.h)
author: windows-sdk-content
description: Enumerates permissions for the objects in a specified metadata scope.
old-location: winrt\imetadataimport_enumpermissionsets.htm
tech.root: WinRT
ms.assetid: 20fec6e8-02f8-4158-8d61-550653e99dad
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EnumPermissionSets, EnumPermissionSets method [Windows Runtime], EnumPermissionSets method [Windows Runtime],IMetaDataImport interface, IMetaDataImport interface [Windows Runtime],EnumPermissionSets method, IMetaDataImport.EnumPermissionSets, IMetaDataImport::EnumPermissionSets, rometadataapi/IMetaDataImport::EnumPermissionSets, winrt.imetadataimport_enumpermissionsets
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
 - IMetaDataImport.EnumPermissionSets
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMetaDataImport::EnumPermissionSets


## -description


Enumerates permissions for the objects in a specified metadata scope.


## -parameters




### -param phEnum [in, out]

A pointer to the enumerator. This must be NULL for the first call of this method.


### -param tk [in]

A metadata token that limits the scope of the search, or NULL to search the widest scope possible.


### -param dwActions [in]

 Flags representing the <a href="http://msdn.microsoft.com/en-us/library/system.security.permissions.securityaction.aspx">SecurityAction</a> values to include in <i>rPermission</i>, or zero to return all actions.


### -param rPermission [out]

The array used to store the Permission tokens.


### -param cMax [in]

The maximum size of the <i>rPermission</i> array.


### -param pcTokens [out]

The number of Permission tokens returned in <i>rPermission</i>.


## -returns



<table>
<tr>
<th>HRESULT</th>
<th>Description</th>
</tr>
<tr>
<td><b>S_OK</b></td>
<td><b>EnumPermissionSets</b> returned successfully.</td>
</tr>
<tr>
<td><b>S_FALSE</b></td>
<td>There are no tokens to enumerate. In this case, <i>pcTokens</i> is 0 (zero).
 

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/5457d9d3-9a43-4e89-a52f-1254662ed92a">IMetaDataImport</a>
 

 

