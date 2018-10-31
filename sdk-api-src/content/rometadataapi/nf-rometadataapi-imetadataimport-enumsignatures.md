---
UID: NF:rometadataapi.IMetaDataImport.EnumSignatures
title: IMetaDataImport::EnumSignatures
author: windows-sdk-content
description: Enumerates Signature tokens representing stand-alone signatures in the current scope.
old-location: winrt\imetadataimport_enumsignatures.htm
tech.root: WinRT
ms.assetid: 311cfa18-6eb5-4872-9a46-3c8dcf901f4f
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: EnumSignatures, EnumSignatures method [Windows Runtime], EnumSignatures method [Windows Runtime],IMetaDataImport interface, IMetaDataImport interface [Windows Runtime],EnumSignatures method, IMetaDataImport.EnumSignatures, IMetaDataImport::EnumSignatures, rometadataapi/IMetaDataImport::EnumSignatures, winrt.imetadataimport_enumsignatures
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
 - IMetaDataImport.EnumSignatures
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMetaDataImport::EnumSignatures


## -description


Enumerates Signature tokens representing stand-alone signatures in the current scope.


## -parameters




### -param phEnum [in, out]

 A pointer to the enumerator. This must be NULL for the first call of this method.


### -param rgSignatures [out]

The array used to store the Signature tokens.


### -param cMax [in]

The maximum size of the <i>rgSignatures</i> array.


### -param pcSignatures [out]

The number of Signature tokens returned in <i>rgSignatures</i>.


## -returns



<table>
<tr>
<th>HRESULT</th>
<th>Description</th>
</tr>
<tr>
<td><b>S_OK</b></td>
<td><b>EnumSignatures</b> returned successfully.</td>
</tr>
<tr>
<td><b>S_FALSE</b></td>
<td>There are no tokens to enumerate. In this case, <i>pcSignatures</i> is 0 (zero).
 

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/5457d9d3-9a43-4e89-a52f-1254662ed92a">IMetaDataImport</a>
 

 

