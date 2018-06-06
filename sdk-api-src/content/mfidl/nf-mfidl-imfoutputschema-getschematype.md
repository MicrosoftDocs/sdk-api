---
UID: NF:mfidl.IMFOutputSchema.GetSchemaType
title: IMFOutputSchema::GetSchemaType
author: windows-sdk-content
description: Retrieves the output protection system that is represented by this object. Output protection systems are identified by GUID value.
old-location: mf\imfoutputschema_getschematype.htm
old-project: medfound
ms.assetid: 6015e636-f1ea-4f4a-85d5-e8e896a0ec3c
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: 6015e636-f1ea-4f4a-85d5-e8e896a0ec3c, GetSchemaType, GetSchemaType method [Media Foundation], GetSchemaType method [Media Foundation],IMFOutputSchema interface, IMFOutputSchema interface [Media Foundation],GetSchemaType method, IMFOutputSchema.GetSchemaType, IMFOutputSchema::GetSchemaType, mf.imfoutputschema_getschematype, mfidl/IMFOutputSchema::GetSchemaType
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MFSensorDeviceMode
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
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
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




<a href="https://msdn.microsoft.com/d0786628-dde9-43a9-8e81-0b0c396ad426">IMFOutputSchema</a>
 

 

