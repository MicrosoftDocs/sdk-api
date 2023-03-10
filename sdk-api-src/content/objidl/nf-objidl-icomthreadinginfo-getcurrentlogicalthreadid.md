---
UID: NF:objidl.IComThreadingInfo.GetCurrentLogicalThreadId
title: IComThreadingInfo::GetCurrentLogicalThreadId (objidl.h)
description: The IComThreadingInfo::GetCurrentLogicalThreadId method (objidl.h) retrieves the GUID of the thread in which the caller is executing.
helpviewer_keywords: ["GetCurrentLogicalThreadId","GetCurrentLogicalThreadId method [COM]","GetCurrentLogicalThreadId method [COM]","IComThreadingInfo interface","IComThreadingInfo interface [COM]","GetCurrentLogicalThreadId method","IComThreadingInfo.GetCurrentLogicalThreadId","IComThreadingInfo::GetCurrentLogicalThreadId","_com_icomthreadinginfo_getcurrentlogicalthreadid","com.icomthreadinginfo_getcurrentlogicalthreadid","objidlbase/IComThreadingInfo::GetCurrentLogicalThreadId"]
old-location: com\icomthreadinginfo_getcurrentlogicalthreadid.htm
tech.root: com
ms.assetid: 780bc94d-19b6-4cc8-b27f-9e38520b0afc
ms.date: 08/12/2022
ms.keywords: GetCurrentLogicalThreadId, GetCurrentLogicalThreadId method [COM], GetCurrentLogicalThreadId method [COM],IComThreadingInfo interface, IComThreadingInfo interface [COM],GetCurrentLogicalThreadId method, IComThreadingInfo.GetCurrentLogicalThreadId, IComThreadingInfo::GetCurrentLogicalThreadId, _com_icomthreadinginfo_getcurrentlogicalthreadid, com.icomthreadinginfo_getcurrentlogicalthreadid, objidlbase/IComThreadingInfo::GetCurrentLogicalThreadId
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IComThreadingInfo::GetCurrentLogicalThreadId
 - objidl/IComThreadingInfo::GetCurrentLogicalThreadId
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - objidlbase.h
api_name:
 - IComThreadingInfo.GetCurrentLogicalThreadId
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

<a href="/windows/desktop/api/objidl/nn-objidl-icomthreadinginfo">IComThreadingInfo</a>
