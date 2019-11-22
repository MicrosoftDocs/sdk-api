---
UID: NF:imapi2.IDiscFormat2RawCD.get_ClientName
title: IDiscFormat2RawCD::get_ClientName (imapi2.h)

description: Retrieves the friendly name of the client.
old-location: imapi\idiscformat2rawcd_get_clientname.htm
tech.root: imapi
ms.assetid: dd706b68-0dde-4a44-b5f5-764fad56844f

ms.date: 12/05/2018
ms.keywords: IDiscFormat2RawCD interface [IMAPI],get_ClientName method, IDiscFormat2RawCD.get_ClientName, IDiscFormat2RawCD::get_ClientName, get_ClientName, get_ClientName method [IMAPI], get_ClientName method [IMAPI],IDiscFormat2RawCD interface, imapi.idiscformat2rawcd_get_clientname, imapi2/IDiscFormat2RawCD::get_ClientName
ms.topic: method
f1_keywords: 
 - "imapi2/IDiscFormat2RawCD.get_ClientName"
dev_langs:
 - c++
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
 - IDiscFormat2RawCD.get_ClientName
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDiscFormat2RawCD::get_ClientName


## -description


Retrieves the friendly name of the client.


## -parameters




### -param value [out]

Name supplied by the client application.


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




<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd">IDiscFormat2RawCD</a>



<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2trackatonce-put_clientname">IDiscFormat2TrackAtOnce::put_ClientName</a>
 

 

