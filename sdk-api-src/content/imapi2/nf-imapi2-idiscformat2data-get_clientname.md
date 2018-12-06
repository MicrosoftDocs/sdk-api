---
UID: NF:imapi2.IDiscFormat2Data.get_ClientName
title: IDiscFormat2Data::get_ClientName
author: windows-sdk-content
description: Retrieves the friendly name of the client.
old-location: imapi\idiscformat2data_get_clientname.htm
tech.root: imapi
ms.assetid: faf5009a-395a-49ed-a0c7-e6bc44f17b7c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDiscFormat2Data interface [IMAPI],get_ClientName method, IDiscFormat2Data.get_ClientName, IDiscFormat2Data::get_ClientName, get_ClientName, get_ClientName method [IMAPI], get_ClientName method [IMAPI],IDiscFormat2Data interface, imapi.idiscformat2data_get_clientname, imapi2/IDiscFormat2Data::get_ClientName
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
 - IDiscFormat2Data.get_ClientName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDiscFormat2Data::get_ClientName


## -description


Retrieves the friendly name of the client.


## -parameters




### -param value [out]

Name of the client application.


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
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Failed to allocate the required memory.

Value: 0x8007000E

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/6bb871c2-1a6e-4cf6-94e1-7a566ce7a88e">IDiscFormat2Data</a>



<a href="https://msdn.microsoft.com/1cd4ef46-4769-4e8e-80ca-fdcd81b486f1">IDiscFormat2Data::put_ClientName</a>
 

 

