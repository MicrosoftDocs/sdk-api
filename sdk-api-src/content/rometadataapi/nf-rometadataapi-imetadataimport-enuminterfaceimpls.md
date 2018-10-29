---
UID: NF:rometadataapi.IMetaDataImport.EnumInterfaceImpls
title: IMetaDataImport::EnumInterfaceImpls
author: windows-sdk-content
description: Enumerates MethodDef tokens representing interface implementations.
old-location: winrt\imetadataimport_enuminterfaceimpls.htm
tech.root: WinRT
ms.assetid: 37f3eada-7719-4303-a9c7-57ee396a5dc5
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: EnumInterfaceImpls, EnumInterfaceImpls method [Windows Runtime], EnumInterfaceImpls method [Windows Runtime],IMetaDataImport interface, IMetaDataImport interface [Windows Runtime],EnumInterfaceImpls method, IMetaDataImport.EnumInterfaceImpls, IMetaDataImport::EnumInterfaceImpls, rometadataapi/IMetaDataImport::EnumInterfaceImpls, winrt.imetadataimport_enuminterfaceimpls
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
 - IMetaDataImport.EnumInterfaceImpls
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMetaDataImport::EnumInterfaceImpls


## -description


Enumerates MethodDef tokens representing interface implementations.


## -parameters




### -param phEnum [in, out]

A pointer to the enumerator.


### -param td [in]

The token of the TypeDef whose MethodDef tokens representing interface implementations are to be enumerated.


### -param rImpls [out]

The array used to store the MethodDef tokens.


### -param cMax [in]

The maximum size of the <i>rImpls</i> array.


### -param pcImpls [out, retval]

The actual number of tokens returned in <i>rImpls</i>.


## -returns



<table>
<tr>
<th>HRESULT</th>
<th>Description</th>
</tr>
<tr>
<td><b>S_OK</b></td>
<td><b>EnumInterfaceImpls</b> returned successfully.</td>
</tr>
<tr>
<td><b>S_FALSE</b></td>
<td>There are no MethodDef tokens to enumerate. In this case, <i>pcImpls</i> is 0 (zero).
 

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/5457d9d3-9a43-4e89-a52f-1254662ed92a">IMetaDataImport</a>
 

 

