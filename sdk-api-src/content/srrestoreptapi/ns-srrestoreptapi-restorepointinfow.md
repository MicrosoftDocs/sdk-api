---
UID: NS:srrestoreptapi._RESTOREPTINFOW
title: RESTOREPOINTINFOW (srrestoreptapi.h)
author: windows-sdk-content
description: Contains information used by the SRSetRestorePoint function.
old-location: sr\restorepointinfo_str.htm
tech.root: sr
ms.assetid: 6f3c1fab-5298-47bb-ba38-87d11f111245
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PRESTOREPOINTINFOW, APPLICATION_INSTALL, APPLICATION_UNINSTALL, BEGIN_NESTED_SYSTEM_CHANGE, BEGIN_SYSTEM_CHANGE, CANCELLED_OPERATION, DEVICE_DRIVER_INSTALL, END_NESTED_SYSTEM_CHANGE, END_SYSTEM_CHANGE, MODIFY_SETTINGS, PRESTOREPOINTINFO, PRESTOREPOINTINFO structure pointer [System Restore], RESTOREPOINTINFO, RESTOREPOINTINFO structure [System Restore], RESTOREPOINTINFOA, RESTOREPOINTINFOW, _sr_restorepointinfo_str, sr.restorepointinfo_str, srrestoreptapi/PRESTOREPOINTINFO, srrestoreptapi/RESTOREPOINTINFO, srrestoreptapi/RESTOREPOINTINFOA, srrestoreptapi/RESTOREPOINTINFOW"
ms.topic: struct
f1_keywords: 
 - "srrestoreptapi/RESTOREPOINTINFO"
req.header: srrestoreptapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RESTOREPOINTINFOW (Unicode) and RESTOREPOINTINFOA (ANSI)
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
 - SRRestorePtAPI.h
api_name:
 - RESTOREPOINTINFO
 - RESTOREPOINTINFOA
 - RESTOREPOINTINFOW
targetos: Windows
req.typenames: RESTOREPOINTINFOW, *PRESTOREPOINTINFOW
req.redist: 
ms.custom: 19H1
---

# RESTOREPOINTINFOW structure


## -description


Contains information used by the 
<a href="https://docs.microsoft.com/windows/desktop/api/srrestoreptapi/nf-srrestoreptapi-srsetrestorepointa">SRSetRestorePoint</a> function.


## -struct-fields




### -field dwEventType

The type of event. This member can be one of the following values. 



<table>
<tr>
<th>Event type</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="BEGIN_NESTED_SYSTEM_CHANGE"></a><a id="begin_nested_system_change"></a><dl>
<dt><b>BEGIN_NESTED_SYSTEM_CHANGE</b></dt>
<dt>102</dt>
</dl>
</td>
<td width="60%">
 A system change has begun. A subsequent nested call does not create a new restore point. 




Subsequent calls must use END_NESTED_SYSTEM_CHANGE, not END_SYSTEM_CHANGE.

</td>
</tr>
<tr>
<td width="40%"><a id="BEGIN_SYSTEM_CHANGE"></a><a id="begin_system_change"></a><dl>
<dt><b>BEGIN_SYSTEM_CHANGE</b></dt>
<dt>100</dt>
</dl>
</td>
<td width="60%">
A system change has begun.

</td>
</tr>
<tr>
<td width="40%"><a id="END_NESTED_SYSTEM_CHANGE"></a><a id="end_nested_system_change"></a><dl>
<dt><b>END_NESTED_SYSTEM_CHANGE</b></dt>
<dt>103</dt>
</dl>
</td>
<td width="60%">
 A system change has ended.

</td>
</tr>
<tr>
<td width="40%"><a id="END_SYSTEM_CHANGE"></a><a id="end_system_change"></a><dl>
<dt><b>END_SYSTEM_CHANGE</b></dt>
<dt>101</dt>
</dl>
</td>
<td width="60%">
A system change has ended.

</td>
</tr>
</table>
 


### -field dwRestorePtType

The type of restore point. This member can be one of the following values. 



<table>
<tr>
<th>Restore point type</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="APPLICATION_INSTALL"></a><a id="application_install"></a><dl>
<dt><b>APPLICATION_INSTALL</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
An application has been installed.

</td>
</tr>
<tr>
<td width="40%"><a id="APPLICATION_UNINSTALL"></a><a id="application_uninstall"></a><dl>
<dt><b>APPLICATION_UNINSTALL</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
An application has been uninstalled.

</td>
</tr>
<tr>
<td width="40%"><a id="DEVICE_DRIVER_INSTALL"></a><a id="device_driver_install"></a><dl>
<dt><b>DEVICE_DRIVER_INSTALL</b></dt>
<dt>10</dt>
</dl>
</td>
<td width="60%">
A device driver has been installed.

</td>
</tr>
<tr>
<td width="40%"><a id="MODIFY_SETTINGS"></a><a id="modify_settings"></a><dl>
<dt><b>MODIFY_SETTINGS</b></dt>
<dt>12</dt>
</dl>
</td>
<td width="60%">
An application has had features added or removed.

</td>
</tr>
<tr>
<td width="40%"><a id="CANCELLED_OPERATION"></a><a id="cancelled_operation"></a><dl>
<dt><b>CANCELLED_OPERATION</b></dt>
<dt>13</dt>
</dl>
</td>
<td width="60%">
An application needs to delete the restore point it created. For example, an application would use this flag when a user cancels an installation.

</td>
</tr>
</table>
 


### -field llSequenceNumber

The sequence number of the restore point. To end a system change, set this to the sequence number returned by the previous call to 
<a href="https://docs.microsoft.com/windows/desktop/api/srrestoreptapi/nf-srrestoreptapi-srsetrestorepointa">SRSetRestorePoint</a>.


### -field szDescription

The description to be displayed so the user can easily identify a restore point. The maximum length of an ANSI string is MAX_DESC. The maximum length of a Unicode string is MAX_DESC_W. For more information, see 
<a href="https://docs.microsoft.com/windows/desktop/sr/restore-point-description-text">Restore Point Description Text</a>.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/srrestoreptapi/nf-srrestoreptapi-srsetrestorepointa">SRSetRestorePoint</a>
 

 

