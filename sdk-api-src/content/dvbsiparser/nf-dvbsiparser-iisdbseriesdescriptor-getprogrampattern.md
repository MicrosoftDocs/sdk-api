---
UID: NF:dvbsiparser.IIsdbSeriesDescriptor.GetProgramPattern
title: IIsdbSeriesDescriptor::GetProgramPattern (dvbsiparser.h)
description: Gets a code that indicates how often a series is programmed from an Integrated Services Digital Broadcasting (ISDB) series descriptor.
helpviewer_keywords: ["GetProgramPattern","GetProgramPattern method [Microsoft TV Technologies]","GetProgramPattern method [Microsoft TV Technologies]","IIsdbSeriesDescriptor interface","IIsdbSeriesDescriptor interface [Microsoft TV Technologies]","GetProgramPattern method","IIsdbSeriesDescriptor.GetProgramPattern","IIsdbSeriesDescriptor::GetProgramPattern","dvbsiparser/IIsdbSeriesDescriptor::GetProgramPattern","mstv.iisdbseriesdescriptor_getprogrampattern"]
old-location: mstv\iisdbseriesdescriptor_getprogrampattern.htm
tech.root: mstv
ms.assetid: ba37c512-bbde-42ad-80fe-9d67f48299b6
ms.date: 12/05/2018
ms.keywords: GetProgramPattern, GetProgramPattern method [Microsoft TV Technologies], GetProgramPattern method [Microsoft TV Technologies],IIsdbSeriesDescriptor interface, IIsdbSeriesDescriptor interface [Microsoft TV Technologies],GetProgramPattern method, IIsdbSeriesDescriptor.GetProgramPattern, IIsdbSeriesDescriptor::GetProgramPattern, dvbsiparser/IIsdbSeriesDescriptor::GetProgramPattern, mstv.iisdbseriesdescriptor_getprogrampattern
req.header: dvbsiparser.h
req.include-header: Dvbsiparser.idl
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
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
 - IIsdbSeriesDescriptor::GetProgramPattern
 - dvbsiparser/IIsdbSeriesDescriptor::GetProgramPattern
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dvbsiparser.h
api_name:
 - IIsdbSeriesDescriptor.GetProgramPattern
---

# IIsdbSeriesDescriptor::GetProgramPattern


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets a code that indicates how often a series is programmed from an Integrated Services Digital Broadcasting (ISDB) series descriptor.

## -parameters

### -param pbVal [out]

Receives the program pattern code. This can be any of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x0</dt>
</dl>
</td>
<td width="60%">
Unscheduled.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x1</dt>
</dl>
</td>
<td width="60%">
Programmed several times weekly.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x2</dt>
</dl>
</td>
<td width="60%">
Programmed once weekly.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x3</dt>
</dl>
</td>
<td width="60%">
Programmed once monthly.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x4</dt>
</dl>
</td>
<td width="60%">
Programmed several times in a single day.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x5</dt>
</dl>
</td>
<td width="60%">
Division of a long program.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x6</dt>
</dl>
</td>
<td width="60%">
Program for regular or irregular accumulation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x7</dt>
</dl>
</td>
<td width="60%">
Undefined.

</td>
</tr>
</table>

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbseriesdescriptor">IIsdbSeriesDescriptor</a>