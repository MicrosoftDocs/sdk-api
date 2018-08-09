---
UID: NF:wsdclient.IWSDMetadataExchange.GetMetadata
title: IWSDMetadataExchange::GetMetadata
author: windows-sdk-content
description: Retrieves metadata for an object.
old-location: ncd\iwsdmetadataexchange_getmetadata_method.htm
old-project: wsdapi
ms.assetid: ab84ed56-37a5-48ff-a616-cb92dc07a8ee
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetMetadata, GetMetadata method, GetMetadata method,IWSDMetadataExchange interface, IWSDMetadataExchange interface,GetMetadata method, IWSDMetadataExchange.GetMetadata, IWSDMetadataExchange::GetMetadata, ncd.iwsdmetadataexchange_getmetadata_method, wsdclient/IWSDMetadataExchange::GetMetadata
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wsdclient.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wsdclient.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WSD_SECURITY_SIGNATURE_VALIDATION, *PWSD_SECURITY_SIGNATURE_VALIDATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wsdapi.dll
api_name:
 - IWSDMetadataExchange.GetMetadata
product: Windows
targetos: Windows
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSDMetadataExchange::GetMetadata


## -description


Retrieves metadata for an object.


## -parameters




### -param MetadataOut [out]

Pointer to a linked list of structures containing the requested metadata.


## -returns



Possible return values include, but are not limited to, the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>MetadataOut</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/f4e2c2f7-3e76-4a17-88f8-9d59c18343a9">IWSDMetadataExchange</a>
 

 

