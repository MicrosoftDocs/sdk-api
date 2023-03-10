---
UID: NF:objidlbase.IComThreadingInfo.SetCurrentLogicalThreadId
title: IComThreadingInfo::SetCurrentLogicalThreadId (objidlbase.h)
description: The IComThreadingInfo::SetCurrentLogicalThreadId (objidlbase.h) method sets the GUID of the thread in which the caller is executing.
helpviewer_keywords: ["IComThreadingInfo interface [COM]","SetCurrentLogicalThreadId method","IComThreadingInfo.SetCurrentLogicalThreadId","IComThreadingInfo::SetCurrentLogicalThreadId","SetCurrentLogicalThreadId","SetCurrentLogicalThreadId method [COM]","SetCurrentLogicalThreadId method [COM]","IComThreadingInfo interface","_com_icomthreadinginfo_setcurrentlogicalthreadid","com.icomthreadinginfo_setcurrentlogicalthreadid","objidlbase/IComThreadingInfo::SetCurrentLogicalThreadId"]
old-location: com\icomthreadinginfo_setcurrentlogicalthreadid.htm
tech.root: com
ms.assetid: 8a2fb319-094e-4384-b520-2cb8b8819d42
ms.date: 08/13/2022
ms.keywords: IComThreadingInfo interface [COM],SetCurrentLogicalThreadId method, IComThreadingInfo.SetCurrentLogicalThreadId, IComThreadingInfo::SetCurrentLogicalThreadId, SetCurrentLogicalThreadId, SetCurrentLogicalThreadId method [COM], SetCurrentLogicalThreadId method [COM],IComThreadingInfo interface, _com_icomthreadinginfo_setcurrentlogicalthreadid, com.icomthreadinginfo_setcurrentlogicalthreadid, objidlbase/IComThreadingInfo::SetCurrentLogicalThreadId
req.header: objidlbase.h
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
 - IComThreadingInfo::SetCurrentLogicalThreadId
 - objidlbase/IComThreadingInfo::SetCurrentLogicalThreadId
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
 - IComThreadingInfo.SetCurrentLogicalThreadId
---

# IComThreadingInfo::SetCurrentLogicalThreadId


## -description

Sets the GUID of the thread in which the caller is executing.

## -parameters

### -param rguid [in]

A reference to a GUID for the caller's thread.

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
