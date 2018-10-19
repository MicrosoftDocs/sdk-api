---
UID: NF:imapi2.IDiscFormat2RawCD.get_LastPossibleStartOfLeadout
title: IDiscFormat2RawCD::get_LastPossibleStartOfLeadout
author: windows-sdk-content
description: Retrieves the last possible starting position for the leadout area.
old-location: imapi\idiscformat2rawcd_get_lastpossiblestartofleadout.htm
tech.root: imapi
ms.assetid: 2588f35e-388b-4491-a209-99d34b1d82df
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: IDiscFormat2RawCD interface [IMAPI],get_LastPossibleStartOfLeadout method, IDiscFormat2RawCD.get_LastPossibleStartOfLeadout, IDiscFormat2RawCD::get_LastPossibleStartOfLeadout, get_LastPossibleStartOfLeadout, get_LastPossibleStartOfLeadout method [IMAPI], get_LastPossibleStartOfLeadout method [IMAPI],IDiscFormat2RawCD interface, imapi.idiscformat2rawcd_get_lastpossiblestartofleadout, imapi2/IDiscFormat2RawCD::get_LastPossibleStartOfLeadout
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
 - IDiscFormat2RawCD.get_LastPossibleStartOfLeadout
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDiscFormat2RawCD::get_LastPossibleStartOfLeadout


## -description


Retrieves the last possible starting position for the leadout area.  


## -parameters




### -param value [out]

Sector address of the starting position for the leadout area.


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
<dt><b>E_IMAPI_DF2RAW_MEDIA_IS_NOT_PREPARED</b></dt>
</dl>
</td>
<td width="60%">
The requested operation is only valid when media has been "prepared".

Value: 0xC0AA0602

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/58d9b83c-a528-4b39-b08d-a0fb8c1aece8">IDiscFormat2RawCD</a>
 

 

