---
UID: NS:ntsecpkg._SECPKG_EVENT_PACKAGE_CHANGE
title: SECPKG_EVENT_PACKAGE_CHANGE (ntsecpkg.h)
description: The SECPKG_EVENT_PACKAGE_CHANGE structure contains information about changes in security package availability.
helpviewer_keywords: ["*PSECPKG_EVENT_PACKAGE_CHANGE","PSECPKG_EVENT_PACKAGE_CHANGE","PSECPKG_EVENT_PACKAGE_CHANGE structure pointer [Security]","SECPKG_EVENT_PACKAGE_CHANGE","SECPKG_EVENT_PACKAGE_CHANGE structure [Security]","SECPKG_PACKAGE_CHANGE_LOAD","SECPKG_PACKAGE_CHANGE_SELECT","SECPKG_PACKAGE_CHANGE_UNLOAD","_ssp_secpkg_event_package_change","ntsecpkg/PSECPKG_EVENT_PACKAGE_CHANGE","ntsecpkg/SECPKG_EVENT_PACKAGE_CHANGE","security.secpkg_event_package_change"]
old-location: security\secpkg_event_package_change.htm
tech.root: security
ms.assetid: fc341828-6491-435e-a20f-c7a4a3c2123d
ms.date: 12/05/2018
ms.keywords: '*PSECPKG_EVENT_PACKAGE_CHANGE, PSECPKG_EVENT_PACKAGE_CHANGE, PSECPKG_EVENT_PACKAGE_CHANGE structure pointer [Security], SECPKG_EVENT_PACKAGE_CHANGE, SECPKG_EVENT_PACKAGE_CHANGE structure [Security], SECPKG_PACKAGE_CHANGE_LOAD, SECPKG_PACKAGE_CHANGE_SELECT, SECPKG_PACKAGE_CHANGE_UNLOAD, _ssp_secpkg_event_package_change, ntsecpkg/PSECPKG_EVENT_PACKAGE_CHANGE, ntsecpkg/SECPKG_EVENT_PACKAGE_CHANGE, security.secpkg_event_package_change'
req.header: ntsecpkg.h
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
req.typenames: SECPKG_EVENT_PACKAGE_CHANGE, *PSECPKG_EVENT_PACKAGE_CHANGE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SECPKG_EVENT_PACKAGE_CHANGE
 - ntsecpkg/_SECPKG_EVENT_PACKAGE_CHANGE
 - PSECPKG_EVENT_PACKAGE_CHANGE
 - ntsecpkg/PSECPKG_EVENT_PACKAGE_CHANGE
 - SECPKG_EVENT_PACKAGE_CHANGE
 - ntsecpkg/SECPKG_EVENT_PACKAGE_CHANGE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntsecpkg.h
api_name:
 - SECPKG_EVENT_PACKAGE_CHANGE
---

# SECPKG_EVENT_PACKAGE_CHANGE structure


## -description

The <b>SECPKG_EVENT_PACKAGE_CHANGE</b> structure contains information about changes in <a href="/windows/desktop/SecGloss/s-gly">security package</a> availability. This structure is indirectly used by the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_register_notification">RegisterNotification</a> function. It is returned to a registered notification function when the function is registered to receive notifications for the <i>NotificationClass</i> parameter value NOTIFY_CLASS_PACKAGE_CHANGE.

## -struct-fields

### -field ChangeType

The type of change. One of the following values will be specified.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SECPKG_PACKAGE_CHANGE_LOAD"></a><a id="secpkg_package_change_load"></a><dl>
<dt><b>SECPKG_PACKAGE_CHANGE_LOAD</b></dt>
</dl>
</td>
<td width="60%">
A package was loaded.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_PACKAGE_CHANGE_UNLOAD"></a><a id="secpkg_package_change_unload"></a><dl>
<dt><b>SECPKG_PACKAGE_CHANGE_UNLOAD</b></dt>
</dl>
</td>
<td width="60%">
A package was unloaded.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_PACKAGE_CHANGE_SELECT"></a><a id="secpkg_package_change_select"></a><dl>
<dt><b>SECPKG_PACKAGE_CHANGE_SELECT</b></dt>
</dl>
</td>
<td width="60%">
A new package became the preferred security package.

</td>
</tr>
</table>

### -field PackageId

The identifier of the security package.

### -field PackageName

The name of the security package.