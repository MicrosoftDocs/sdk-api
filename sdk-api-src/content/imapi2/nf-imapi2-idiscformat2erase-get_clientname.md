---
UID: NF:imapi2.IDiscFormat2Erase.get_ClientName
title: IDiscFormat2Erase::get_ClientName
author: windows-sdk-content
description: Retrieves the friendly name of the client.
old-location: imapi\idiscformat2erase_get_clientname.htm
old-project: imapi
ms.assetid: be52c76d-3c6a-44b7-a948-4d0b02a7a7bb
ms.author: windowssdkdev
ms.date: 06/15/2018
ms.keywords: IDiscFormat2Erase interface [IMAPI],get_ClientName method, IDiscFormat2Erase.get_ClientName, IDiscFormat2Erase::get_ClientName, get_ClientName, get_ClientName method [IMAPI], get_ClientName method [IMAPI],IDiscFormat2Erase interface, imapi.idiscformat2erase_get_clientname, imapi2/IDiscFormat2Erase::get_ClientName
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: IMAPI_READ_TRACK_ADDRESS_TYPE, *PIMAPI_READ_TRACK_ADDRESS_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2.h
api_name:
 - IDiscFormat2Erase.get_ClientName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IDiscFormat2Erase::get_ClientName


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




<a href="https://msdn.microsoft.com/3789c876-f42c-4f69-b683-96c157d6418d">IDiscFormat2Erase</a>



<a href="https://msdn.microsoft.com/641395b1-724b-42d1-b230-a4d6f3844077">IDiscFormat2Erase::put_ClientName</a>
 

 

