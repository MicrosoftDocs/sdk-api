---
UID: NF:dvbsiparser.IIsdbDigitalCopyControlDescriptor.GetCopyControl
title: IIsdbDigitalCopyControlDescriptor::GetCopyControl
author: windows-sdk-content
description: Gets copy control data from an Integrated Services Digital Broadcasting (ISDB) digital copy control descriptor.
old-location: mstv\iisdbdigitalcopycontroldescriptor_getcopycontrol.htm
old-project: mstv
ms.assetid: 115ed5f7-a445-4ff2-a9d7-035867b2504d
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetCopyControl, GetCopyControl method [Microsoft TV Technologies], GetCopyControl method [Microsoft TV Technologies],IIsdbDigitalCopyControlDescriptor interface, IIsdbDigitalCopyControlDescriptor interface [Microsoft TV Technologies],GetCopyControl method, IIsdbDigitalCopyControlDescriptor.GetCopyControl, IIsdbDigitalCopyControlDescriptor::GetCopyControl, dvbsiparser/IIsdbDigitalCopyControlDescriptor::GetCopyControl, mstv.iisdbdigitalcopycontroldescriptor_getcopycontrol
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
req.typenames: DSROLE_UPGRADE_STATUS_INFO, *PDSROLE_UPGRADE_STATUS_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dvbsiparser.h
api_name:
-	IIsdbDigitalCopyControlDescriptor.GetCopyControl
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IIsdbDigitalCopyControlDescriptor::GetCopyControl


## -description


Gets copy control data from an Integrated Services Digital Broadcasting (ISDB) digital copy control descriptor.


## -parameters




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
Output with pseudosync pulse.

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

Receives the maximum trasmission rate for transport stream packets, in units of 250 kbps.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/d509eb58-0c58-4173-8c9c-d52b81932b5c">IIsdbDigitalCopyControlDescriptor</a>
 

 

