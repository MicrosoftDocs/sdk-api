---
UID: NF:dvbsiparser.IIsdbDigitalCopyControlDescriptor.GetRecordCopyControl
title: IIsdbDigitalCopyControlDescriptor::GetRecordCopyControl (dvbsiparser.h)
description: Gets copy control data from a specified component in an Integrated Services Digital Broadcasting (ISDB) digital copy control descriptor.
helpviewer_keywords: ["GetRecordCopyControl","GetRecordCopyControl method [Microsoft TV Technologies]","GetRecordCopyControl method [Microsoft TV Technologies]","IIsdbDigitalCopyControlDescriptor interface","IIsdbDigitalCopyControlDescriptor interface [Microsoft TV Technologies]","GetRecordCopyControl method","IIsdbDigitalCopyControlDescriptor.GetRecordCopyControl","IIsdbDigitalCopyControlDescriptor::GetRecordCopyControl","dvbsiparser/IIsdbDigitalCopyControlDescriptor::GetRecordCopyControl","mstv.iisdbdigitalcopycontroldescriptor_getrecordcopycontrol"]
old-location: mstv\iisdbdigitalcopycontroldescriptor_getrecordcopycontrol.htm
tech.root: mstv
ms.assetid: 800e2263-b04a-4030-9aba-c0b38033b82d
ms.date: 12/05/2018
ms.keywords: GetRecordCopyControl, GetRecordCopyControl method [Microsoft TV Technologies], GetRecordCopyControl method [Microsoft TV Technologies],IIsdbDigitalCopyControlDescriptor interface, IIsdbDigitalCopyControlDescriptor interface [Microsoft TV Technologies],GetRecordCopyControl method, IIsdbDigitalCopyControlDescriptor.GetRecordCopyControl, IIsdbDigitalCopyControlDescriptor::GetRecordCopyControl, dvbsiparser/IIsdbDigitalCopyControlDescriptor::GetRecordCopyControl, mstv.iisdbdigitalcopycontroldescriptor_getrecordcopycontrol
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
 - IIsdbDigitalCopyControlDescriptor::GetRecordCopyControl
 - dvbsiparser/IIsdbDigitalCopyControlDescriptor::GetRecordCopyControl
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
 - IIsdbDigitalCopyControlDescriptor.GetRecordCopyControl
---

# IIsdbDigitalCopyControlDescriptor::GetRecordCopyControl


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets copy control data from a specified component in an Integrated Services Digital Broadcasting (ISDB) digital copy control descriptor. When the component_control_flag field in the descriptor is set to 1, the control information is specified in each component of the descriptor.

## -parameters

### -param bRecordIndex [in]

Specifies the record number for the component,
  indexed from zero. Call the <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbdigitalcopycontroldescriptor-getcountofrecords">IIsdbDigitalCompyControlDescriptor::GetCountOfRecords</a> method to get the number of records in the digital copy control descriptor.

### -param pbComponentTag [out]

Receives  the tag identifying the component. This value is the same as the 	component tag in the stream
identifier descriptor and the component descriptor.

### -param pbDigitalRecordingControlData [out]

Receives the two-bit code that indicates the type of copy control. This code can have any of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>00</dt>
</dl>
</td>
<td width="60%">
Unrestricted copies allowed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>01</dt>
</dl>
</td>
<td width="60%">
When <i>pbCopyControlType</i> parameter is 11, not used; when <i>pbCopyControlType</i> is 01, copying forbidden.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>10</dt>
</dl>
</td>
<td width="60%">
Can be copied only once.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>11</dt>
</dl>
</td>
<td width="60%">
Copying forbidden.

</td>
</tr>
</table>

### -param pbCopyControlType [out]

Receives data that defines output control options for digital copying.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>00</dt>
</dl>
</td>
<td width="60%">
Undefined.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>01</dt>
</dl>
</td>
<td width="60%">
Output by encoding to serial interface.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>10</dt>
</dl>
</td>
<td width="60%">
Undefined.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>11</dt>
</dl>
</td>
<td width="60%">
Output by not encoding to serial interface.

</td>
</tr>
</table>

### -param pbAPSControlData [out]

Receives data that defines output control options for analog copying when the value of the <i>pbCopyControlType</i> parameter is 01.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>00</dt>
</dl>
</td>
<td width="60%">
Undefined.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>01</dt>
</dl>
</td>
<td width="60%">
Output with pseudosync pulse

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>10</dt>
</dl>
</td>
<td width="60%">
Output with pseudosync pulse + two-line reversed division burst insertion.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>11</dt>
</dl>
</td>
<td width="60%">
Output with pseudosync pulse + four-line reversed division burst insertion.

</td>
</tr>
</table>

### -param pbMaximumBitrate [out]

Receives the maximum transmission rate for transport stream packets, in units of 250 kbps.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbdigitalcopycontroldescriptor-getcountofrecords">IIsdbDigitalCompyControlDescriptor::GetCountOfRecords</a>



<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbdigitalcopycontroldescriptor">IIsdbDigitalCopyControlDescriptor</a>