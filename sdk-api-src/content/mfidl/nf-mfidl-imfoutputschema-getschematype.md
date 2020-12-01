---
UID: NF:mfidl.IMFOutputSchema.GetSchemaType
title: IMFOutputSchema::GetSchemaType (mfidl.h)
description: Retrieves the output protection system that is represented by this object. Output protection systems are identified by GUID value.
helpviewer_keywords: ["6015e636-f1ea-4f4a-85d5-e8e896a0ec3c","GetSchemaType","GetSchemaType method [Media Foundation]","GetSchemaType method [Media Foundation]","IMFOutputSchema interface","IMFOutputSchema interface [Media Foundation]","GetSchemaType method","IMFOutputSchema.GetSchemaType","IMFOutputSchema::GetSchemaType","mf.imfoutputschema_getschematype","mfidl/IMFOutputSchema::GetSchemaType"]
old-location: mf\imfoutputschema_getschematype.htm
tech.root: mf
ms.assetid: 6015e636-f1ea-4f4a-85d5-e8e896a0ec3c
ms.date: 12/05/2018
ms.keywords: 6015e636-f1ea-4f4a-85d5-e8e896a0ec3c, GetSchemaType, GetSchemaType method [Media Foundation], GetSchemaType method [Media Foundation],IMFOutputSchema interface, IMFOutputSchema interface [Media Foundation],GetSchemaType method, IMFOutputSchema.GetSchemaType, IMFOutputSchema::GetSchemaType, mf.imfoutputschema_getschematype, mfidl/IMFOutputSchema::GetSchemaType
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFOutputSchema::GetSchemaType
 - mfidl/IMFOutputSchema::GetSchemaType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFOutputSchema.GetSchemaType
---

# IMFOutputSchema::GetSchemaType


## -description

Retrieves the output protection system that is represented by this object. Output protection systems are identified by GUID value.

## -parameters

### -param pguidSchemaType [out]

Receives the GUID that identifies the output protection system.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfoutputschema">IMFOutputSchema</a>