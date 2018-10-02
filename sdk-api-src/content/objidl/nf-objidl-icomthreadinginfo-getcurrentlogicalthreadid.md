---
UID: NF:objidl.IComThreadingInfo.GetCurrentLogicalThreadId
title: IComThreadingInfo::GetCurrentLogicalThreadId
author: windows-sdk-content
description: Retrieves the GUID of the thread in which the caller is executing.
old-location: com\icomthreadinginfo_getcurrentlogicalthreadid.htm
tech.root: com
ms.assetid: 780bc94d-19b6-4cc8-b27f-9e38520b0afc
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: GetCurrentLogicalThreadId, GetCurrentLogicalThreadId method [COM], GetCurrentLogicalThreadId method [COM],IComThreadingInfo interface, IComThreadingInfo interface [COM],GetCurrentLogicalThreadId method, IComThreadingInfo.GetCurrentLogicalThreadId, IComThreadingInfo::GetCurrentLogicalThreadId, _com_icomthreadinginfo_getcurrentlogicalthreadid, com.icomthreadinginfo_getcurrentlogicalthreadid, objidlbase/IComThreadingInfo::GetCurrentLogicalThreadId
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
 - IComThreadingInfo.GetCurrentLogicalThreadId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IComThreadingInfo::GetCurrentLogicalThreadId


## -description


Retrieves the GUID of the thread in which the caller is executing.


## -parameters




### -param pguidLogicalThreadId [out]

A pointer to the GUID of the caller's thread.


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
 

 

