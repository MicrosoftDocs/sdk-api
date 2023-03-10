---
UID: NF:oaidl.ICreateErrorInfo.SetGUID
title: ICreateErrorInfo::SetGUID (oaidl.h)
description: Sets the globally unique identifier (GUID) of the interface that defined the error.
helpviewer_keywords: ["ICreateErrorInfo interface [Automation]","SetGUID method","ICreateErrorInfo.SetGUID","ICreateErrorInfo::SetGUID","SetGUID","SetGUID method [Automation]","SetGUID method [Automation]","ICreateErrorInfo interface","_oa96_ICreateErrorInfo_SetGUID","automat.icreateerrorinfo_setguid","oaidl/ICreateErrorInfo::SetGUID"]
old-location: automat\icreateerrorinfo_setguid.htm
tech.root: automat
ms.assetid: f7570ba3-d738-40d3-aefc-fbf6f4ca633e
ms.date: 12/05/2018
ms.keywords: ICreateErrorInfo interface [Automation],SetGUID method, ICreateErrorInfo.SetGUID, ICreateErrorInfo::SetGUID, SetGUID, SetGUID method [Automation], SetGUID method [Automation],ICreateErrorInfo interface, _oa96_ICreateErrorInfo_SetGUID, automat.icreateerrorinfo_setguid, oaidl/ICreateErrorInfo::SetGUID
req.header: oaidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OaIdl.idl
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
 - ICreateErrorInfo::SetGUID
 - oaidl/ICreateErrorInfo::SetGUID
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - oaidl.h
api_name:
 - ICreateErrorInfo.SetGUID
---

# ICreateErrorInfo::SetGUID


## -description

Sets the globally unique identifier (GUID) of the interface that defined the error.

## -parameters

### -param rguid [in]

The GUID of the interface that defined the error, or GUID_NULL if the error was defined by the operating system.

## -returns

This method can return one of these values.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to complete the operation.


</td>
</tr>
</table>

## -remarks

This method sets the GUID of the interface that defined the error. If the error was defined by the system, set <b>ICreateErrorInfo::SetGUID</b> to GUID_NULL.



This GUID does not necessarily represent the source of the error; however, the source is the class or application that raised the error. Using the GUID, applications can handle errors in an interface, independent of the class that implements the interface.

Use of this function is demonstrated in the file Main.cpp of the COM Fundamentals Hello sample.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-icreateerrorinfo">ICreateErrorInfo</a>