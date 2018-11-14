---
UID: NF:imapi2.IWriteSpeedDescriptor.get_MediaType
title: IWriteSpeedDescriptor::get_MediaType
author: windows-sdk-content
description: Retrieves type of media in the current drive.
old-location: imapi\iwritespeeddescriptor_get_mediatype.htm
tech.root: imapi
ms.assetid: 4608fb27-8d8c-4ccc-9838-bdbe9dadee83
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: IWriteSpeedDescriptor interface [IMAPI],get_MediaType method, IWriteSpeedDescriptor.get_MediaType, IWriteSpeedDescriptor::get_MediaType, get_MediaType, get_MediaType method [IMAPI], get_MediaType method [IMAPI],IWriteSpeedDescriptor interface, imapi.iwritespeeddescriptor_get_mediatype, imapi2/IWriteSpeedDescriptor::get_MediaType
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: imapi2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2.idl
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
 - imapi2.h
api_name:
 - IWriteSpeedDescriptor.get_MediaType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- imapi2.h
: 
- IWriteSpeedDescriptor.get_MediaType
: 
---

# IWriteSpeedDescriptor::get_MediaType


## -description


Retrieves type of media in the current drive.


## -parameters




### -param value [out]

Type of media in the current drive. For possible values, see the <a href="https://msdn.microsoft.com/027c5e09-6cf7-4d7c-8381-07dc92cc43c5">IMAPI_MEDIA_PHYSICAL_TYPE</a> enumeration type.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Pointer is not valid.

Value: 0x80004003

</td>
</tr>
</table>
 




## -see-also




IMAPI_MEDIA_PHYSICAL_TYPE



<a href="https://msdn.microsoft.com/9efaa744-ae0c-4101-8d78-091cba990533">IWriteSpeedDescriptor</a>
 

 

