---
UID: NF:imapi2.IDiscFormat2Data.get_LastWrittenAddressOfPreviousSession
title: IDiscFormat2Data::get_LastWrittenAddressOfPreviousSession
author: windows-sdk-content
description: Retrieves the last sector of the previous write session.
old-location: imapi\idiscformat2data_get_lastwrittenaddressofprevioussession.htm
tech.root: imapi
ms.assetid: cfc9ba42-25a2-49a3-8047-7aaf331332ad
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IDiscFormat2Data interface [IMAPI],get_LastWrittenAddressOfPreviousSession method, IDiscFormat2Data.get_LastWrittenAddressOfPreviousSession, IDiscFormat2Data::get_LastWrittenAddressOfPreviousSession, get_LastWrittenAddressOfPreviousSession, get_LastWrittenAddressOfPreviousSession method [IMAPI], get_LastWrittenAddressOfPreviousSession method [IMAPI],IDiscFormat2Data interface, imapi.idiscformat2data_get_lastwrittenaddressofprevioussession, imapi2/IDiscFormat2Data::get_LastWrittenAddressOfPreviousSession
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
 - IDiscFormat2Data.get_LastWrittenAddressOfPreviousSession
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDiscFormat2Data::get_LastWrittenAddressOfPreviousSession


## -description


Retrieves the last sector of the previous write session.


## -parameters




### -param value [out]

  Address where the previous write operation ended.  

The value is -1 if the media is blank or does not support multi-session writing (indicates that no previous session could be detected).


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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Not implemented.

Value: 0x80004001

</td>
</tr>
</table>
 




## -remarks



<div class="alert"><b>Note</b>  This property should not be used. Instead, you should use an interface derived from <a href="https://msdn.microsoft.com/a983af02-ee0e-4a62-8ae0-fb9a1e0c2571">IMultisession</a>, such as <a href="https://msdn.microsoft.com/b8124597-e75a-4f95-a25c-8cf59f452548">IMultisessionSequential</a>, for importing file data from the previous session.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/6bb871c2-1a6e-4cf6-94e1-7a566ce7a88e">IDiscFormat2Data</a>



<a href="https://msdn.microsoft.com/bdbab74c-80bd-4dca-8d64-6d30452a5876">IDiscFormat2Data::get_NextWritableAddress</a>



<a href="https://msdn.microsoft.com/a2f75240-9334-42a3-82d6-5ce9ddf1f3a2">IDiscFormat2Data::get_StartAddressOfPreviousSession</a>
 

 

