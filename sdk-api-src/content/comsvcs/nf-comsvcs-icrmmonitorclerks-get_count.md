---
UID: NF:comsvcs.ICrmMonitorClerks.get_Count
title: ICrmMonitorClerks::get_Count
author: windows-sdk-content
description: Retrieves the count of CRM clerks in the collection.
old-location: cos\icrmmonitorclerks_get_count.htm
tech.root: cossdk
ms.assetid: 677f39e5-6f77-46a5-9429-682c0d2933df
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ICrmMonitorClerks interface [COM+],get_Count method, ICrmMonitorClerks.get_Count, ICrmMonitorClerks::get_Count, _dtc_ICrmMonitorClerks_Count, comsvcs/ICrmMonitorClerks::get_Count, cos.icrmmonitorclerks_get_count, get_Count, get_Count method [COM+], get_Count method [COM+],ICrmMonitorClerks interface
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - ComSvcs.h
api_name:
 - ICrmMonitorClerks.get_Count
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- comsvcs.h
: 
- ICrmMonitorClerks.get_Count
: 
---

# ICrmMonitorClerks::get_Count


## -description


Retrieves the count of CRM clerks in the collection.


## -parameters




### -param pVal [out]

The number of CRM clerks.


## -returns



This method can return the following values.

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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A <b>NULL</b> pointer was provided as an argument.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms684207(v=VS.85).aspx">ICrmMonitorClerks</a>
 

 

