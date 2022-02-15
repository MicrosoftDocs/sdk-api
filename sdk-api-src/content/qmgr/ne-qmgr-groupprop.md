---
UID: NE:qmgr.GROUPPROP
title: GROUPPROP (qmgr.h)
description: The GROUPPROP enumeration defines the constant values for retrieving and setting group property values.
helpviewer_keywords: ["GROUPPROP","GROUPPROP enumeration [BITS]","GROUPPROP_DESCRIPTION","GROUPPROP_DISPLAYNAME","GROUPPROP_LOCALUSERID","GROUPPROP_LOCALUSERPWD","GROUPPROP_NOTIFYCLSID","GROUPPROP_NOTIFYFLAGS","GROUPPROP_PRIORITY","GROUPPROP_PROGRESSPERCENT","GROUPPROP_PROGRESSSIZE","GROUPPROP_PROGRESSTIME","GROUPPROP_PROTOCOLFLAGS","GROUPPROP_REMOTEUSERID","GROUPPROP_REMOTEUSERPWD","bits.groupprop","qmgr/GROUPPROP","qmgr/GROUPPROP_DESCRIPTION","qmgr/GROUPPROP_DISPLAYNAME","qmgr/GROUPPROP_LOCALUSERID","qmgr/GROUPPROP_LOCALUSERPWD","qmgr/GROUPPROP_NOTIFYCLSID","qmgr/GROUPPROP_NOTIFYFLAGS","qmgr/GROUPPROP_PRIORITY","qmgr/GROUPPROP_PROGRESSPERCENT","qmgr/GROUPPROP_PROGRESSSIZE","qmgr/GROUPPROP_PROGRESSTIME","qmgr/GROUPPROP_PROTOCOLFLAGS","qmgr/GROUPPROP_REMOTEUSERID","qmgr/GROUPPROP_REMOTEUSERPWD"]
old-location: bits\groupprop.htm
tech.root: Bits
ms.assetid: 8bd5d1df-237a-4c42-afe1-6540ab1ad8c1
ms.date: 12/05/2018
ms.keywords: GROUPPROP, GROUPPROP enumeration [BITS], GROUPPROP_DESCRIPTION, GROUPPROP_DISPLAYNAME, GROUPPROP_LOCALUSERID, GROUPPROP_LOCALUSERPWD, GROUPPROP_NOTIFYCLSID, GROUPPROP_NOTIFYFLAGS, GROUPPROP_PRIORITY, GROUPPROP_PROGRESSPERCENT, GROUPPROP_PROGRESSSIZE, GROUPPROP_PROGRESSTIME, GROUPPROP_PROTOCOLFLAGS, GROUPPROP_REMOTEUSERID, GROUPPROP_REMOTEUSERPWD, bits.groupprop, qmgr/GROUPPROP, qmgr/GROUPPROP_DESCRIPTION, qmgr/GROUPPROP_DISPLAYNAME, qmgr/GROUPPROP_LOCALUSERID, qmgr/GROUPPROP_LOCALUSERPWD, qmgr/GROUPPROP_NOTIFYCLSID, qmgr/GROUPPROP_NOTIFYFLAGS, qmgr/GROUPPROP_PRIORITY, qmgr/GROUPPROP_PROGRESSPERCENT, qmgr/GROUPPROP_PROGRESSSIZE, qmgr/GROUPPROP_PROGRESSTIME, qmgr/GROUPPROP_PROTOCOLFLAGS, qmgr/GROUPPROP_REMOTEUSERID, qmgr/GROUPPROP_REMOTEUSERPWD
req.header: qmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Qmgr.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: GROUPPROP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GROUPPROP
 - qmgr/GROUPPROP
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Qmgr.h
api_name:
 - GROUPPROP
---

# GROUPPROP enumeration


## -description

<p class="CCE_Message">[Queue Manager (QMGR) is available for use in the operating systems specified in the Requirements section.  It may be altered or unavailable in subsequent versions. Instead, use the <a href="/windows/desktop/Bits/background-intelligent-transfer-service-portal">Background Intelligent Transfer Service (BITS)</a>.]

The <b>GROUPPROP</b> enumeration defines the constant values for retrieving and setting group property values.

## -enum-fields

### -field GROUPPROP_PRIORITY:0

Determines when the QMGR processes the group relative to other groups in the queue.

There is only one priority. You must specify a value of 1 when setting this property. The property always returns a value of 1.

Variant data type can be VT_I4, VT_I2, VT_UI4, VT_UI2, VT_INT, or VT_UINT.

### -field GROUPPROP_REMOTEUSERID:1

Not supported.

### -field GROUPPROP_REMOTEUSERPWD:2

Not supported.

### -field GROUPPROP_LOCALUSERID:3

Not supported.

### -field GROUPPROP_LOCALUSERPWD:4

Not supported.

### -field GROUPPROP_PROTOCOLFLAGS:5

Specifies the protocol to use for the download.

You must specify QM_PROTOCOL_HTTP when setting this property.

Variant data type can be VT_I4, VT_I2, VT_UI4, VT_UI2, VT_INT, or VT_UINT.

### -field GROUPPROP_NOTIFYFLAGS:6

Specifies the type of event notification to receive for the group. See Remarks.

Variant data type can be VT_I4, VT_I2, VT_UI4, VT_UI2, VT_INT, or VT_UINT.

### -field GROUPPROP_NOTIFYCLSID:7

The 	CLSID to activate when an event specified by <b>GROUPPROP_NOTIFYFLAGS</b> occurs. For more details on CLSID activation, see <a href="/windows/desktop/api/qmgr/nn-qmgr-ibackgroundcopycallback1">IBackgroundCopyCallback1</a>.

Variant data type is VT_BSTR.

### -field GROUPPROP_PROGRESSSIZE:8

Not supported.

### -field GROUPPROP_PROGRESSPERCENT:9

Not supported.

### -field GROUPPROP_PROGRESSTIME:10

Not supported.

### -field GROUPPROP_DISPLAYNAME:11

Specifies a display name that can be used to identify the group in a user interface. The length of the string is limited to 256 characters, not including the null terminator.

Variant data type is VT_BSTR.

### -field GROUPPROP_DESCRIPTION:12

Specifies a description to associate with the group. The length of the string is limited to 1,024 characters, not including the null terminator.

Variant data type is VT_BSTR.

## -remarks

The <b>GROUPPROP_NOTIFYFLAGS</b> group property can contain one or more of the following notification flags. 

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td>QM_NOTIFY_FILE_DONE</td>
<td>Not supported.</td>
</tr>
<tr>
<td>QM_NOTIFY_JOB_DONE</td>
<td>Not supported.</td>
</tr>
<tr>
<td>QM_NOTIFY_GROUP_DONE</td>
<td>Notifies the application through <a href="/windows/desktop/api/qmgr/nf-qmgr-ibackgroundcopycallback1-onstatus">IBackgroundCopyCallback1::OnStatus</a> that the group is complete.</td>
</tr>
<tr>
<td>QM_NOTIFY_DISABLE_NOTIFY</td>
<td>Disables all notifications.</td>
</tr>
<tr>
<td>QM_NOTIFY_USE_PROGRESSEX</td>
<td>Not supported.</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  By default, QMGR calls your <a href="/windows/desktop/api/qmgr/nf-qmgr-ibackgroundcopycallback1-onstatus">IBackgroundCopyCallback1::OnStatus</a> method when an error occurs.</div>
<div> </div>
