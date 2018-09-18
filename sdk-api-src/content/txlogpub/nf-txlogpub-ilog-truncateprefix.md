---
UID: NF:txlogpub.ILog.TruncatePrefix
title: ILog::TruncatePrefix
author: windows-sdk-content
description: Throws away the specified prefix of the log, making it no longer retrievable.
old-location: com\ilog_truncateprefix.htm
tech.root: com
ms.assetid: 079c05b3-19ad-401d-ad5c-1095e897799f
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: ILog interface [COM],TruncatePrefix method, ILog.TruncatePrefix, ILog::TruncatePrefix, TruncatePrefix, TruncatePrefix method [COM], TruncatePrefix method [COM],ILog interface, _com_ilog_truncateprefix, com.ilog_truncateprefix, txlogpub/ILog::TruncatePrefix
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: txlogpub.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Txlogpub.idl
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
 - Txlogpub.h
api_name:
 - ILog.TruncatePrefix
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ILog::TruncatePrefix


## -description


Throws away the specified prefix of the log, making it no longer retrievable.


## -parameters




### -param lsnFirstToKeep [in]

The LSN of the first record not to be thrown away. If this parameter is 0, the entire log is emptied.


## -returns



This method can return the following values, as well as other <b>HRESULT</b> values.

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
The log was successfully truncated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>lsnFirstToKeep</i> is outside the current limits of the log. See <a href="https://msdn.microsoft.com/06238436-6807-4588-9af9-03eb4c12f4e1">ILog::GetLogLimits</a>.

</td>
</tr>
</table>
 




## -remarks



This request is only a hint to the log implementation. The log is free to ignore the request, or to retain more than was strictly requested. Many <a href="https://msdn.microsoft.com/93f2be99-0799-4047-ae4e-62f0e74d15c3">ILog</a> implementations will follow this latter option.




## -see-also




<a href="https://msdn.microsoft.com/93f2be99-0799-4047-ae4e-62f0e74d15c3">ILog</a>
 

 

