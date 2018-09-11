---
UID: NF:encdec.IDTFilter3.GetProtectionType
title: IDTFilter3::GetProtectionType
author: windows-sdk-content
description: The GetProtectionType method retrieves the type of content protection that is currently in effect.
old-location: mstv\idtfilter3_getprotectiontype.htm
tech.root: mstv
ms.assetid: 6b1e4186-de85-4de8-b309-82644c8b1269
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetProtectionType, GetProtectionType method [Microsoft TV Technologies], GetProtectionType method [Microsoft TV Technologies],IDTFilter3 interface, IDTFilter3 interface [Microsoft TV Technologies],GetProtectionType method, IDTFilter3.GetProtectionType, IDTFilter3::GetProtectionType, IDTFilter3GetProtectionType, encdec/IDTFilter3::GetProtectionType, mstv.idtfilter3_getprotectiontype
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: encdec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - encdec.h
api_name:
 - IDTFilter3.GetProtectionType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDTFilter3::GetProtectionType


## -description


The <b>GetProtectionType</b> method retrieves the type of content protection that is currently in effect.


## -parameters




### -param pProtectionType [out]

Receives the current protection type, specified as a member of the <a href="https://msdn.microsoft.com/190b8483-91c8-4fe4-8189-637749393151">ProtType</a> enumeration type.


## -returns



Returns an <b>HRESULT</b>. Possible values include the following.

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
Success.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/88e42006-c387-41b5-a013-e968da0d918b">IDTFilter3 Interface</a>
 

 

