---
UID: NF:winsync.IClockVector.GetClockVectorElements
title: IClockVector::GetClockVectorElements (winsync.h)
description: Returns an enumerator that iterates through the clock vector elements.
helpviewer_keywords: ["GetClockVectorElements","GetClockVectorElements method [Windows Sync]","GetClockVectorElements method [Windows Sync]","IClockVector interface","IClockVector interface [Windows Sync]","GetClockVectorElements method","IClockVector.GetClockVectorElements","IClockVector::GetClockVectorElements","winsync.iclockvector_getclockvectorelements","winsync/IClockVector::GetClockVectorElements"]
old-location: winsync\iclockvector_getclockvectorelements.htm
tech.root: winsync
ms.assetid: a0712a2b-5aeb-458d-bc0f-c18eeb7ba9ff
ms.date: 12/05/2018
ms.keywords: GetClockVectorElements, GetClockVectorElements method [Windows Sync], GetClockVectorElements method [Windows Sync],IClockVector interface, IClockVector interface [Windows Sync],GetClockVectorElements method, IClockVector.GetClockVectorElements, IClockVector::GetClockVectorElements, winsync.iclockvector_getclockvectorelements, winsync/IClockVector::GetClockVectorElements
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
 - IClockVector::GetClockVectorElements
 - winsync/IClockVector::GetClockVectorElements
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
 - IClockVector.GetClockVectorElements
---

# IClockVector::GetClockVectorElements


## -description

Returns an enumerator that iterates through the clock vector elements.

## -parameters

### -param riid [in]

The IID of the enumeration interface that is requested. Must be either <b>IID_IEnumClockVector</b> or <b>IID_IEnumFeedClockVector</b>.

### -param ppiEnumClockVector [out]

Returns an object that implements <i>riid</i> and that can enumerate the clock vector elements.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Invalid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
<i>riid</i> is not  <b>IID_IEnumClockVector</b> or <b>IID_IEnumFeedClockVector</b>.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-iclockvector">IClockVector Interface</a>