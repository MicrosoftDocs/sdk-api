---
UID: NS:ntmsapi._NTMS_OPREQUESTINFORMATIONA
title: NTMS_OPREQUESTINFORMATIONA (ntmsapi.h)
description: The NTMS_OPREQUESTINFORMATION structure defines the properties specific to operator-request system control for RSM. (ANSI)
helpviewer_keywords: ["NTMS_CHANGER","NTMS_DRIVE","NTMS_IEDOOR","NTMS_IEPORT.","NTMS_LIBRARY","NTMS_OPREQUESTINFORMATION","NTMS_OPREQUESTINFORMATION structure [Files]","NTMS_OPREQUESTINFORMATIONA","NTMS_OPREQUESTINFORMATIONW","NTMS_OPREQ_CLEANER","NTMS_OPREQ_DEVICESERVICE","NTMS_OPREQ_MESSAGE","NTMS_OPREQ_MOVEMEDIA","NTMS_OPREQ_NEWMEDIA","NTMS_OPSTATE_ACTIVE","NTMS_OPSTATE_COMPLETE","NTMS_OPSTATE_INPROGRESS","NTMS_OPSTATE_REFUSED","NTMS_OPSTATE_SUBMITTED","NTMS_PARTITION","NTMS_PHYSICAL_MEDIA","NTMS_STORAGESLOT","NTMS_UNKNOWN","_NTMS_OPREQUESTINFORMATIONA","_NTMS_OPREQUESTINFORMATIONW","_zaw_ntms_oprequestinformation","base.ntms_oprequestinformation","fs.ntms_oprequestinformation","ntmsapi/NTMS_OPREQUESTINFORMATION"]
old-location: fs\ntms_oprequestinformation.htm
tech.root: fs
ms.assetid: d6ff9240-8f58-4f2e-9298-ff2f0193eeba
ms.date: 12/05/2018
ms.keywords: NTMS_CHANGER, NTMS_DRIVE, NTMS_IEDOOR, NTMS_IEPORT., NTMS_LIBRARY, NTMS_OPREQUESTINFORMATION, NTMS_OPREQUESTINFORMATION structure [Files], NTMS_OPREQUESTINFORMATIONA, NTMS_OPREQUESTINFORMATIONW, NTMS_OPREQ_CLEANER, NTMS_OPREQ_DEVICESERVICE, NTMS_OPREQ_MESSAGE, NTMS_OPREQ_MOVEMEDIA, NTMS_OPREQ_NEWMEDIA, NTMS_OPSTATE_ACTIVE, NTMS_OPSTATE_COMPLETE, NTMS_OPSTATE_INPROGRESS, NTMS_OPSTATE_REFUSED, NTMS_OPSTATE_SUBMITTED, NTMS_PARTITION, NTMS_PHYSICAL_MEDIA, NTMS_STORAGESLOT, NTMS_UNKNOWN, _NTMS_OPREQUESTINFORMATIONA, _NTMS_OPREQUESTINFORMATIONW, _zaw_ntms_oprequestinformation, base.ntms_oprequestinformation, fs.ntms_oprequestinformation, ntmsapi/NTMS_OPREQUESTINFORMATION
req.header: ntmsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: NTMS_OPREQUESTINFORMATIONA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _NTMS_OPREQUESTINFORMATIONA
 - ntmsapi/_NTMS_OPREQUESTINFORMATIONA
 - NTMS_OPREQUESTINFORMATIONA
 - ntmsapi/NTMS_OPREQUESTINFORMATIONA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntmsapi.h
api_name:
 - NTMS_OPREQUESTINFORMATION
 - NTMS_OPREQUESTINFORMATIONA
 - NTMS_OPREQUESTINFORMATIONW
---

# NTMS_OPREQUESTINFORMATIONA structure


## -description

<p class="CCE_Message">[<a href="/previous-versions/windows/desktop/bb540725(v=vs.85)">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>NTMS_OPREQUESTINFORMATION</b> structure defines the properties specific to operator-request system control for RSM.

## -struct-fields

### -field Request

Type of operator request. This can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NTMS_OPREQ_NEWMEDIA"></a><a id="ntms_opreq_newmedia"></a><dl>
<dt><b>NTMS_OPREQ_NEWMEDIA</b></dt>
</dl>
</td>
<td width="60%">
An application attempting to allocate media sends an operator request for new media when no media is available. When this flag is set, the <b>Arg1</b> member should be set to the GUID of the media pool requiring new media. Optionally, the <b>Arg2</b> member can be set to the particular library in which the new media should be placed.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_OPREQ_CLEANER"></a><a id="ntms_opreq_cleaner"></a><dl>
<dt><b>NTMS_OPREQ_CLEANER</b></dt>
</dl>
</td>
<td width="60%">
RSM sends an operator request for a cleaner when a clean operation is queued and no cleaner is online and available to the drive. When this flag is set, the <b>Arg1</b> member should be set to the GUID of the library requiring the cleaning cartridge.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_OPREQ_DEVICESERVICE"></a><a id="ntms_opreq_deviceservice"></a><dl>
<dt><b>NTMS_OPREQ_DEVICESERVICE</b></dt>
</dl>
</td>
<td width="60%">
An application or RSM sends an operator request for drive service when a changer device or drive is experiencing problems. When this flag is set, the <b>Arg1</b> member should be set to the GUID of the device requiring service.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_OPREQ_MOVEMEDIA"></a><a id="ntms_opreq_movemedia"></a><dl>
<dt><b>NTMS_OPREQ_MOVEMEDIA</b></dt>
</dl>
</td>
<td width="60%">
An application or RSM sends an operator request to move the specified medium to service a mount for offline media or to eject media to an offline library. When this flag is set, the <b>Arg1</b> member should be set to the GUID of the physical media to move and the <b>Arg2</b> member should be set to the GUID of the library this media should be moved to.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_OPREQ_MESSAGE"></a><a id="ntms_opreq_message"></a><dl>
<dt><b>NTMS_OPREQ_MESSAGE</b></dt>
</dl>
</td>
<td width="60%">
An application-specific operator request. Text only.

</td>
</tr>
</table>

### -field Submitted

System time when the operator request was submitted.

### -field State

Current state of the operator service request. This can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NTMS_OPSTATE_SUBMITTED"></a><a id="ntms_opstate_submitted"></a><dl>
<dt><b>NTMS_OPSTATE_SUBMITTED</b></dt>
</dl>
</td>
<td width="60%">
The operator request has been submitted but not read by an operator console.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_OPSTATE_ACTIVE"></a><a id="ntms_opstate_active"></a><dl>
<dt><b>NTMS_OPSTATE_ACTIVE</b></dt>
</dl>
</td>
<td width="60%">
The operator request has been read by one or more operator consoles and might be in process.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_OPSTATE_INPROGRESS"></a><a id="ntms_opstate_inprogress"></a><dl>
<dt><b>NTMS_OPSTATE_INPROGRESS</b></dt>
</dl>
</td>
<td width="60%">
The user has acknowledged this operator request and is in the process of performing the service.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_OPSTATE_REFUSED"></a><a id="ntms_opstate_refused"></a><dl>
<dt><b>NTMS_OPSTATE_REFUSED</b></dt>
</dl>
</td>
<td width="60%">
The user has rejected the operator service request.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_OPSTATE_COMPLETE"></a><a id="ntms_opstate_complete"></a><dl>
<dt><b>NTMS_OPSTATE_COMPLETE</b></dt>
</dl>
</td>
<td width="60%">
The user has completed the operator service request.

</td>
</tr>
</table>

### -field szMessage

Operator message text.

### -field Arg1Type

Type of the <b>Arg1</b> object. This can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NTMS_UNKNOWN"></a><a id="ntms_unknown"></a><dl>
<dt><b>NTMS_UNKNOWN</b></dt>
</dl>
</td>
<td width="60%">
No object provided in <b>Arg1Type</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_CHANGER"></a><a id="ntms_changer"></a><dl>
<dt><b>NTMS_CHANGER</b></dt>
</dl>
</td>
<td width="60%">
Medium changer object.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_DRIVE"></a><a id="ntms_drive"></a><dl>
<dt><b>NTMS_DRIVE</b></dt>
</dl>
</td>
<td width="60%">
Drive object.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_IEDOOR"></a><a id="ntms_iedoor"></a><dl>
<dt><b>NTMS_IEDOOR</b></dt>
</dl>
</td>
<td width="60%">
Library door object.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_IEPORT."></a><a id="ntms_ieport."></a><dl>
<dt><b>NTMS_IEPORT.</b></dt>
</dl>
</td>
<td width="60%">
Library insert/eject port object

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_LIBRARY"></a><a id="ntms_library"></a><dl>
<dt><b>NTMS_LIBRARY</b></dt>
</dl>
</td>
<td width="60%">
Library object.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_PARTITION"></a><a id="ntms_partition"></a><dl>
<dt><b>NTMS_PARTITION</b></dt>
</dl>
</td>
<td width="60%">
Side object.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_PHYSICAL_MEDIA"></a><a id="ntms_physical_media"></a><dl>
<dt><b>NTMS_PHYSICAL_MEDIA</b></dt>
</dl>
</td>
<td width="60%">
Physical media object.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_STORAGESLOT"></a><a id="ntms_storageslot"></a><dl>
<dt><b>NTMS_STORAGESLOT</b></dt>
</dl>
</td>
<td width="60%">
Library slot object.

</td>
</tr>
</table>

### -field Arg1

<b>Arg1</b> object ID used for move requests or other operator requests that require a reference object. The purpose of this object varies based on the type of operator request. For appropriate uses of <b>Arg1</b>, see the <b>Request</b> description.

### -field Arg2Type

Type of <b>Arg2</b> object. This can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NTMS_UNKNOWN"></a><a id="ntms_unknown"></a><dl>
<dt><b>NTMS_UNKNOWN</b></dt>
</dl>
</td>
<td width="60%">
No object provided in <b>Arg2Type</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_LIBRARY"></a><a id="ntms_library"></a><dl>
<dt><b>NTMS_LIBRARY</b></dt>
</dl>
</td>
<td width="60%">
Library object.

</td>
</tr>
</table>

### -field Arg2

<b>Arg2</b> object ID used for operator requests that require a second reference object. The purpose of this object varies based on the type of operator request. For appropriate uses of <b>Arg2</b>, see the <b>Request</b> description.

### -field szApplication

Application that submitted the operator request.

### -field szUser

Interactive user logged on to the computer that submitted the operator request.

### -field szComputer

Computer that submitted the operator request.

## -remarks

The 
<b>NTMS_OPREQUESTINFORMATION</b> structure is included in the 
<a href="/windows/desktop/api/ntmsapi/ns-ntmsapi-ntms_objectinformationa">NTMS_OBJECTINFORMATION</a> structure.





> [!NOTE]
> The ntmsapi.h header defines NTMS_OPREQUESTINFORMATION as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/ntmsapi/ns-ntmsapi-ntms_objectinformationa">NTMS_OBJECTINFORMATION</a>
