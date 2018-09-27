---
UID: NF:objidl.IComThreadingInfo.GetCurrentThreadType
title: IComThreadingInfo::GetCurrentThreadType
author: windows-sdk-content
description: Retrieves the type of thread in which the caller is executing.
old-location: com\icomthreadinginfo_getcurrentthreadtype.htm
tech.root: com
ms.assetid: 93437e45-f1e7-4f1f-bffb-ef234c7f5a6b
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: GetCurrentThreadType, GetCurrentThreadType method [COM], GetCurrentThreadType method [COM],IComThreadingInfo interface, IComThreadingInfo interface [COM],GetCurrentThreadType method, IComThreadingInfo.GetCurrentThreadType, IComThreadingInfo::GetCurrentThreadType, _com_icomthreadinginfo_getcurrentthreadtype, com.icomthreadinginfo_getcurrentthreadtype, objidlbase/IComThreadingInfo::GetCurrentThreadType
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: objidl.h
req.include-header: ObjIdl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
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
 - objidlbase.h
api_name:
 - IComThreadingInfo.GetCurrentThreadType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IComThreadingInfo::GetCurrentThreadType


## -description


Retrieves the type of thread in which the caller is executing.


## -parameters




### -param pThreadType [out]

A pointer to a <a href="https://msdn.microsoft.com/c1f9ab7b-8915-4433-ae9f-57b1aedcad4d">THDTYPE</a> enumeration value that characterizes the caller's thread.


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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The caller is not executing in an apartment.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/fa4c7d82-ec5d-43d6-914e-bba60ad19aa2">IComThreadingInfo</a>
 

 

