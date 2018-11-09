---
UID: NS:tapi.linecallstatus_tag
title: linecallstatus_tag
author: windows-sdk-content
description: The LINECALLSTATUS structure describes the current status of a call.
old-location: tapi2\linecallstatus_str.htm
tech.root: tapi
ms.assetid: f056bea6-aeb0-4c18-8e3b-c1c6fd907f62
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: "*LPLINECALLSTATUS, LINECALLSTATE_BUSY, LINECALLSTATE_CONNECTED, LINECALLSTATE_DIALTONE, LINECALLSTATE_DISCONNECTED, LINECALLSTATE_OFFERING, LINECALLSTATE_SPECIALINFO, LINECALLSTATUS, LINECALLSTATUS structure [TAPI 2.2], LPLINECALLSTATUS, LPLINECALLSTATUS structure pointer [TAPI 2.2], _tapi2_linecallstatus_str, linecallstatus_tag, tapi/LINECALLSTATUS, tapi/LPLINECALLSTATUS, tapi2.linecallstatus_str"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: tapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tapi.h
api_name:
 - LINECALLSTATUS
product: Windows
targetos: Windows
req.typenames: LINECALLSTATUS, *LPLINECALLSTATUS
req.redist: 
---

# linecallstatus_tag structure


## -description


The 
<b>LINECALLSTATUS</b> structure describes the current status of a call. The information in this structure depends on the device capabilities of the address, the ownership of the call by the invoking application, and the current state of the call being queried. The 
<a href="https://msdn.microsoft.com/88bcd211-0993-4703-b43f-4e0b93e3eb7e">lineGetCallStatus</a> and 
<a href="https://msdn.microsoft.com/7124ef73-148f-41df-afd6-ebfa29d5cf1c">TSPI_lineGetCallStatus</a> functions return the 
<b>LINECALLSTATUS</b> structure.


## -struct-fields




### -field dwTotalSize

Total size allocated to this data structure, in bytes.


### -field dwNeededSize

Size for this data structure that is needed to hold all the returned information, in bytes.


### -field dwUsedSize

Size of the portion of this data structure that contains useful information, in bytes.


### -field dwCallState

Current call state of the call using one of the 
<a href="https://msdn.microsoft.com/18d881ee-cf98-4dec-a561-333c2518935d">LINECALLSTATE_ constants</a>.


### -field dwCallStateMode

Interpretation of the <b>dwCallStateMode</b> member is call-state-dependent. In many cases, the value will be zero. The following table shows <b>dwCallStateMode</b> types for a given <b>dwCallState</b> value. 



<table>
<tr>
<th>dwCallState</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LINECALLSTATE_BUSY"></a><a id="linecallstate_busy"></a><dl>
<dt><b>LINECALLSTATE_BUSY</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/4a3fa79f-7a7a-4f9b-9353-e6c5ca4fcb4e">LINEBUSYMODE_ Constants</a>


</td>
</tr>
<tr>
<td width="40%"><a id="LINECALLSTATE_CONNECTED"></a><a id="linecallstate_connected"></a><dl>
<dt><b>LINECALLSTATE_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/d75a5989-3f4e-4e5d-90b1-4e450def017e">LINECONNECTEDMODE_ Constants</a>


</td>
</tr>
<tr>
<td width="40%"><a id="LINECALLSTATE_DIALTONE"></a><a id="linecallstate_dialtone"></a><dl>
<dt><b>LINECALLSTATE_DIALTONE</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/0b040482-35cf-42e8-84bc-33002635b591">LINEDIALTONEMODE_ Constants</a>


</td>
</tr>
<tr>
<td width="40%"><a id="LINECALLSTATE_DISCONNECTED"></a><a id="linecallstate_disconnected"></a><dl>
<dt><b>LINECALLSTATE_DISCONNECTED</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/1b26f13c-b0bf-4d2c-8514-f0c376e36bcd">LINEDISCONNECTMODE_ Constants</a>


</td>
</tr>
<tr>
<td width="40%"><a id="LINECALLSTATE_OFFERING"></a><a id="linecallstate_offering"></a><dl>
<dt><b>LINECALLSTATE_OFFERING</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/a6c6d30f-fdc4-4ba5-b1a2-3c709445aedc">LINEOFFERINGMODE_ Constants</a>


</td>
</tr>
<tr>
<td width="40%"><a id="LINECALLSTATE_SPECIALINFO"></a><a id="linecallstate_specialinfo"></a><dl>
<dt><b>LINECALLSTATE_SPECIALINFO</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/b94f8a6f-b84d-4976-b4d4-10dee5a1a4d8">LINESPECIALINFO_ Constants</a>


</td>
</tr>
</table>
 


### -field dwCallPrivilege

Application's privilege for this call. This member uses one or more of the 
<a href="https://msdn.microsoft.com/a58b7e9e-696e-4421-9b31-1ba8afe6e03b">LINECALLPRIVILEGE_ constants</a>.


### -field dwCallFeatures

Flags that indicate the Telephony API functions that can be invoked on the call, given the availability of the feature in the device capabilities, the current call state, and call ownership of the invoking application. A zero indicates the corresponding feature cannot be invoked by the application on the call in its current state; a one indicates the feature can be invoked. This member uses 
<a href="https://msdn.microsoft.com/8bb1d678-079c-4c83-b4a2-08fd7afdca9b">LINECALLFEATURE_ Constants</a>.


### -field dwDevSpecificSize

Size of the device-specific field, in bytes.


### -field dwDevSpecificOffset

Offset from the beginning of the structure to the variably sized device-specific field. The size of the field is specified by <b>dwDevSpecificOffset</b>.


### -field dwCallFeatures2

Indicates additional functions can be invoked on the call, given the availability of the feature in the device capabilities, the current call state, and call ownership of the invoking application. An extension of the <b>dwCallFeatures</b> member. This member uses 
<a href="https://msdn.microsoft.com/67a3b587-dd5b-4ccf-ab69-2137604706b8">LINECALLFEATURE2_ Constants</a>.


### -field tStateEntryTime

Coordinated Universal Time at which the current call state was entered.


## -remarks



Device-specific extensions should use the DevSpecific (<b>dwDevSpecificSize</b> and <b>dwDevSpecificOffset</b>) variably sized area of this data structure.

The application is sent a 
<a href="https://msdn.microsoft.com/7b24e3c3-bc69-488b-a698-cf17875bc3c5">LINE_CALLSTATE</a> message whenever the call state of a call changes. This message only provides the new call state of the call. Additional status about a call is available with 
<a href="https://msdn.microsoft.com/88bcd211-0993-4703-b43f-4e0b93e3eb7e">lineGetCallStatus</a>.

The members <b>dwCallFeatures2</b> and <b>tStateEntryTime</b> are available only to applications that open the line device with an API version of 2.0 or later.




## -see-also




<a href="https://msdn.microsoft.com/efb65462-abe5-46db-9299-97871e0d011e">LINEDIALPARAMS</a>



<a href="https://msdn.microsoft.com/7b24e3c3-bc69-488b-a698-cf17875bc3c5">LINE_CALLSTATE</a>



<a href="https://msdn.microsoft.com/7124ef73-148f-41df-afd6-ebfa29d5cf1c">TSPI_lineGetCallStatus</a>



<a href="https://msdn.microsoft.com/88bcd211-0993-4703-b43f-4e0b93e3eb7e">lineGetCallStatus</a>
 

 

