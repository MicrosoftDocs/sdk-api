---
UID: NF:winsync.IChangeUnitException.GetClockVector
title: IChangeUnitException::GetClockVector (winsync.h)
description: Gets the clock vector that is associated with this exception. (IChangeUnitException.GetClockVector)
helpviewer_keywords: ["GetClockVector","GetClockVector method [Windows Sync]","GetClockVector method [Windows Sync]","IChangeUnitException interface","IChangeUnitException interface [Windows Sync]","GetClockVector method","IChangeUnitException.GetClockVector","IChangeUnitException::GetClockVector","winsync.ichangeunitexception_getclockvector","winsync/IChangeUnitException::GetClockVector"]
old-location: winsync\ichangeunitexception_getclockvector.htm
tech.root: winsync
ms.assetid: 1cf95acf-23ab-49c8-bd63-7aff9bad8f25
ms.date: 12/05/2018
ms.keywords: GetClockVector, GetClockVector method [Windows Sync], GetClockVector method [Windows Sync],IChangeUnitException interface, IChangeUnitException interface [Windows Sync],GetClockVector method, IChangeUnitException.GetClockVector, IChangeUnitException::GetClockVector, winsync.ichangeunitexception_getclockvector, winsync/IChangeUnitException::GetClockVector
req.header: winsync.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IChangeUnitException::GetClockVector
 - winsync/IChangeUnitException::GetClockVector
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - winsync.h
api_name:
 - IChangeUnitException.GetClockVector
---

# IChangeUnitException::GetClockVector


## -description

Gets the clock vector that is associated with this exception.

## -parameters

### -param riid [in]

The IID of the object to retrieve. Must be <b>IID_IEnumClockVector</b>.

### -param ppUnk [out]

Returns an object that implements <i>riid</i> and that represents the clock vector that is associated with this exception.

## -returns

The possible return codes include, but are not limited to, the values shown in the following table.

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
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-ichangeunitexception">IChangeUnitException Interface</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-ienumclockvector">IEnumClockVector Interface</a>
