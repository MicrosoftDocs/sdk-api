---
UID: NS:winsvc._SERVICE_CONTROL_STATUS_REASON_PARAMSW
title: SERVICE_CONTROL_STATUS_REASON_PARAMSW (winsvc.h)
description: Contains service control parameters. (Unicode)
helpviewer_keywords: ["*PSERVICE_CONTROL_STATUS_REASON_PARAMSW","PSERVICE_CONTROL_STATUS_REASON_PARAMS","PSERVICE_CONTROL_STATUS_REASON_PARAMS structure pointer","SERVICE_CONTROL_STATUS_REASON_PARAMS","SERVICE_CONTROL_STATUS_REASON_PARAMS structure","SERVICE_CONTROL_STATUS_REASON_PARAMSA","SERVICE_CONTROL_STATUS_REASON_PARAMSW","SERVICE_STOP_REASON_FLAG_CUSTOM","SERVICE_STOP_REASON_FLAG_PLANNED","SERVICE_STOP_REASON_FLAG_UNPLANNED","SERVICE_STOP_REASON_MAJOR_APPLICATION","SERVICE_STOP_REASON_MAJOR_HARDWARE","SERVICE_STOP_REASON_MAJOR_NONE","SERVICE_STOP_REASON_MAJOR_OPERATINGSYSTEM","SERVICE_STOP_REASON_MAJOR_OTHER","SERVICE_STOP_REASON_MAJOR_SOFTWARE","SERVICE_STOP_REASON_MINOR_DISK","SERVICE_STOP_REASON_MINOR_ENVIRONMENT","SERVICE_STOP_REASON_MINOR_HARDWARE_DRIVER","SERVICE_STOP_REASON_MINOR_HUNG","SERVICE_STOP_REASON_MINOR_INSTALLATION","SERVICE_STOP_REASON_MINOR_MAINTENANCE","SERVICE_STOP_REASON_MINOR_MMC","SERVICE_STOP_REASON_MINOR_NETWORKCARD","SERVICE_STOP_REASON_MINOR_NETWORK_CONNECTIVITY","SERVICE_STOP_REASON_MINOR_NONE","SERVICE_STOP_REASON_MINOR_OTHER","SERVICE_STOP_REASON_MINOR_OTHERDRIVER","SERVICE_STOP_REASON_MINOR_RECONFIG","SERVICE_STOP_REASON_MINOR_SECURITY","SERVICE_STOP_REASON_MINOR_SECURITYFIX","SERVICE_STOP_REASON_MINOR_SECURITYFIX_UNINSTALL","SERVICE_STOP_REASON_MINOR_SERVICEPACK","SERVICE_STOP_REASON_MINOR_SERVICEPACK_UNINSTALL","SERVICE_STOP_REASON_MINOR_SOFTWARE_UPDATE","SERVICE_STOP_REASON_MINOR_SOFTWARE_UPDATE_UNINSTALL","SERVICE_STOP_REASON_MINOR_UNSTABLE","SERVICE_STOP_REASON_MINOR_UPGRADE","SERVICE_STOP_REASON_MINOR_WMI","base.service_control_status_reason_params","winsvc/PSERVICE_CONTROL_STATUS_REASON_PARAMS","winsvc/SERVICE_CONTROL_STATUS_REASON_PARAMS","winsvc/SERVICE_CONTROL_STATUS_REASON_PARAMSA","winsvc/SERVICE_CONTROL_STATUS_REASON_PARAMSW"]
old-location: base\service_control_status_reason_params.htm
tech.root: security
ms.assetid: f7213cbb-255f-4ce3-93c9-5537256e078f
ms.date: 12/05/2018
ms.keywords: '*PSERVICE_CONTROL_STATUS_REASON_PARAMSW, PSERVICE_CONTROL_STATUS_REASON_PARAMS, PSERVICE_CONTROL_STATUS_REASON_PARAMS structure pointer, SERVICE_CONTROL_STATUS_REASON_PARAMS, SERVICE_CONTROL_STATUS_REASON_PARAMS structure, SERVICE_CONTROL_STATUS_REASON_PARAMSA, SERVICE_CONTROL_STATUS_REASON_PARAMSW, SERVICE_STOP_REASON_FLAG_CUSTOM, SERVICE_STOP_REASON_FLAG_PLANNED, SERVICE_STOP_REASON_FLAG_UNPLANNED, SERVICE_STOP_REASON_MAJOR_APPLICATION, SERVICE_STOP_REASON_MAJOR_HARDWARE, SERVICE_STOP_REASON_MAJOR_NONE, SERVICE_STOP_REASON_MAJOR_OPERATINGSYSTEM, SERVICE_STOP_REASON_MAJOR_OTHER, SERVICE_STOP_REASON_MAJOR_SOFTWARE, SERVICE_STOP_REASON_MINOR_DISK, SERVICE_STOP_REASON_MINOR_ENVIRONMENT, SERVICE_STOP_REASON_MINOR_HARDWARE_DRIVER, SERVICE_STOP_REASON_MINOR_HUNG, SERVICE_STOP_REASON_MINOR_INSTALLATION, SERVICE_STOP_REASON_MINOR_MAINTENANCE, SERVICE_STOP_REASON_MINOR_MMC, SERVICE_STOP_REASON_MINOR_NETWORKCARD, SERVICE_STOP_REASON_MINOR_NETWORK_CONNECTIVITY, SERVICE_STOP_REASON_MINOR_NONE, SERVICE_STOP_REASON_MINOR_OTHER, SERVICE_STOP_REASON_MINOR_OTHERDRIVER, SERVICE_STOP_REASON_MINOR_RECONFIG, SERVICE_STOP_REASON_MINOR_SECURITY, SERVICE_STOP_REASON_MINOR_SECURITYFIX, SERVICE_STOP_REASON_MINOR_SECURITYFIX_UNINSTALL, SERVICE_STOP_REASON_MINOR_SERVICEPACK, SERVICE_STOP_REASON_MINOR_SERVICEPACK_UNINSTALL, SERVICE_STOP_REASON_MINOR_SOFTWARE_UPDATE, SERVICE_STOP_REASON_MINOR_SOFTWARE_UPDATE_UNINSTALL, SERVICE_STOP_REASON_MINOR_UNSTABLE, SERVICE_STOP_REASON_MINOR_UPGRADE, SERVICE_STOP_REASON_MINOR_WMI, base.service_control_status_reason_params, winsvc/PSERVICE_CONTROL_STATUS_REASON_PARAMS, winsvc/SERVICE_CONTROL_STATUS_REASON_PARAMS, winsvc/SERVICE_CONTROL_STATUS_REASON_PARAMSA, winsvc/SERVICE_CONTROL_STATUS_REASON_PARAMSW'
req.header: winsvc.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SERVICE_CONTROL_STATUS_REASON_PARAMSW (Unicode) and SERVICE_CONTROL_STATUS_REASON_PARAMSA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SERVICE_CONTROL_STATUS_REASON_PARAMSW, *PSERVICE_CONTROL_STATUS_REASON_PARAMSW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SERVICE_CONTROL_STATUS_REASON_PARAMSW
 - winsvc/_SERVICE_CONTROL_STATUS_REASON_PARAMSW
 - PSERVICE_CONTROL_STATUS_REASON_PARAMSW
 - winsvc/PSERVICE_CONTROL_STATUS_REASON_PARAMSW
 - SERVICE_CONTROL_STATUS_REASON_PARAMSW
 - winsvc/SERVICE_CONTROL_STATUS_REASON_PARAMSW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winsvc.h
api_name:
 - SERVICE_CONTROL_STATUS_REASON_PARAMS
 - SERVICE_CONTROL_STATUS_REASON_PARAMSA
 - SERVICE_CONTROL_STATUS_REASON_PARAMSW
---

# SERVICE_CONTROL_STATUS_REASON_PARAMSW structure


## -description

Contains service control parameters.

## -struct-fields

### -field dwReason

The reason for changing the service status to SERVICE_CONTROL_STOP. If the current control code is not SERVICE_CONTROL_STOP, this member is ignored. 

This member must be set to a combination of one general code, one major reason code, and one minor reason code.


The following are the general reason codes.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SERVICE_STOP_REASON_FLAG_CUSTOM"></a><a id="service_stop_reason_flag_custom"></a><dl>
<dt><b>SERVICE_STOP_REASON_FLAG_CUSTOM</b></dt>
<dt>0x20000000</dt>
</dl>
</td>
<td width="60%">
The reason code is defined by the user. If this flag is not present, the reason code is defined by the system. If this flag is specified with a system reason code, the function call fails. 

Users can create custom major reason codes in the range SERVICE_STOP_REASON_MAJOR_MIN_CUSTOM (0x00400000) through SERVICE_STOP_REASON_MAJOR_MAX_CUSTOM  (0x00ff0000) and minor reason codes in the range SERVICE_STOP_REASON_MINOR_MIN_CUSTOM (0x00000100) through SERVICE_STOP_REASON_MINOR_MAX_CUSTOM (0x0000FFFF).

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_STOP_REASON_FLAG_PLANNED"></a><a id="service_stop_reason_flag_planned"></a><dl>
<dt><b>SERVICE_STOP_REASON_FLAG_PLANNED</b></dt>
<dt>0x40000000</dt>
</dl>
</td>
<td width="60%">
The service stop was planned.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_STOP_REASON_FLAG_UNPLANNED"></a><a id="service_stop_reason_flag_unplanned"></a><dl>
<dt><b>SERVICE_STOP_REASON_FLAG_UNPLANNED</b></dt>
<dt>0x10000000</dt>
</dl>
</td>
<td width="60%">
The service stop was not planned.

</td>
</tr>
</table>
 


The following are the major reason codes.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SERVICE_STOP_REASON_MAJOR_APPLICATION"></a><a id="service_stop_reason_major_application"></a><dl>
<dt><b>SERVICE_STOP_REASON_MAJOR_APPLICATION</b></dt>
<dt>0x00050000</dt>
</dl>
</td>
<td width="60%">
Application issue.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_STOP_REASON_MAJOR_HARDWARE"></a><a id="service_stop_reason_major_hardware"></a><dl>
<dt><b>SERVICE_STOP_REASON_MAJOR_HARDWARE</b></dt>
<dt>0x00020000</dt>
</dl>
</td>
<td width="60%">
Hardware issue.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_STOP_REASON_MAJOR_NONE"></a><a id="service_stop_reason_major_none"></a><dl>
<dt><b>SERVICE_STOP_REASON_MAJOR_NONE</b></dt>
<dt>0x00060000</dt>
</dl>
</td>
<td width="60%">
No major reason.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_STOP_REASON_MAJOR_OPERATINGSYSTEM"></a><a id="service_stop_reason_major_operatingsystem"></a><dl>
<dt><b>SERVICE_STOP_REASON_MAJOR_OPERATINGSYSTEM</b></dt>
<dt>0x00030000</dt>
</dl>
</td>
<td width="60%">
Operating system issue.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_STOP_REASON_MAJOR_OTHER"></a><a id="service_stop_reason_major_other"></a><dl>
<dt><b>SERVICE_STOP_REASON_MAJOR_OTHER</b></dt>
<dt>0x00010000</dt>
</dl>
</td>
<td width="60%">
Other issue.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_STOP_REASON_MAJOR_SOFTWARE"></a><a id="service_stop_reason_major_software"></a><dl>
<dt><b>SERVICE_STOP_REASON_MAJOR_SOFTWARE</b></dt>
<dt>0x00040000</dt>
</dl>
</td>
<td width="60%">
Software issue.

</td>
</tr>
</table>
 


The following are the minor reason codes.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SERVICE_STOP_REASON_MINOR_DISK"></a><a id="service_stop_reason_minor_disk"></a><dl>
<dt><b>SERVICE_STOP_REASON_MINOR_DISK</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
Disk.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_STOP_REASON_MINOR_ENVIRONMENT"></a><a id="service_stop_reason_minor_environment"></a><dl>
<dt><b>SERVICE_STOP_REASON_MINOR_ENVIRONMENT</b></dt>
<dt>0x0000000a</dt>
</dl>
</td>
<td width="60%">
Environment.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_STOP_REASON_MINOR_HARDWARE_DRIVER"></a><a id="service_stop_reason_minor_hardware_driver"></a><dl>
<dt><b>SERVICE_STOP_REASON_MINOR_HARDWARE_DRIVER</b></dt>
<dt>0x0000000b</dt>
</dl>
</td>
<td width="60%">
Driver.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_STOP_REASON_MINOR_HUNG"></a><a id="service_stop_reason_minor_hung"></a><dl>
<dt><b>SERVICE_STOP_REASON_MINOR_HUNG</b></dt>
<dt>0x00000006</dt>
</dl>
</td>
<td width="60%">
Unresponsive.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_STOP_REASON_MINOR_INSTALLATION"></a><a id="service_stop_reason_minor_installation"></a><dl>
<dt><b>SERVICE_STOP_REASON_MINOR_INSTALLATION</b></dt>
<dt>0x00000003</dt>
</dl>
</td>
<td width="60%">
Installation.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_STOP_REASON_MINOR_MAINTENANCE"></a><a id="service_stop_reason_minor_maintenance"></a><dl>
<dt><b>SERVICE_STOP_REASON_MINOR_MAINTENANCE</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Maintenance.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_STOP_REASON_MINOR_MMC"></a><a id="service_stop_reason_minor_mmc"></a><dl>
<dt><b>SERVICE_STOP_REASON_MINOR_MMC</b></dt>
<dt>0x00000016</dt>
</dl>
</td>
<td width="60%">
MMC issue.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_STOP_REASON_MINOR_NETWORK_CONNECTIVITY"></a><a id="service_stop_reason_minor_network_connectivity"></a><dl>
<dt><b>SERVICE_STOP_REASON_MINOR_NETWORK_CONNECTIVITY</b></dt>
<dt>0x00000011</dt>
</dl>
</td>
<td width="60%">
Network connectivity.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_STOP_REASON_MINOR_NETWORKCARD"></a><a id="service_stop_reason_minor_networkcard"></a><dl>
<dt><b>SERVICE_STOP_REASON_MINOR_NETWORKCARD</b></dt>
<dt>0x00000009</dt>
</dl>
</td>
<td width="60%">
Network card.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_STOP_REASON_MINOR_NONE"></a><a id="service_stop_reason_minor_none"></a><dl>
<dt><b>SERVICE_STOP_REASON_MINOR_NONE</b></dt>
<dt>0x00060000</dt>
</dl>
</td>
<td width="60%">
No minor reason.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_STOP_REASON_MINOR_OTHER"></a><a id="service_stop_reason_minor_other"></a><dl>
<dt><b>SERVICE_STOP_REASON_MINOR_OTHER</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Other issue.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_STOP_REASON_MINOR_OTHERDRIVER"></a><a id="service_stop_reason_minor_otherdriver"></a><dl>
<dt><b>SERVICE_STOP_REASON_MINOR_OTHERDRIVER</b></dt>
<dt>0x0000000c</dt>
</dl>
</td>
<td width="60%">
Other driver event.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_STOP_REASON_MINOR_RECONFIG"></a><a id="service_stop_reason_minor_reconfig"></a><dl>
<dt><b>SERVICE_STOP_REASON_MINOR_RECONFIG</b></dt>
<dt>0x00000005</dt>
</dl>
</td>
<td width="60%">
Reconfigure.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_STOP_REASON_MINOR_SECURITY"></a><a id="service_stop_reason_minor_security"></a><dl>
<dt><b>SERVICE_STOP_REASON_MINOR_SECURITY</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
Security issue.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_STOP_REASON_MINOR_SECURITYFIX"></a><a id="service_stop_reason_minor_securityfix"></a><dl>
<dt><b>SERVICE_STOP_REASON_MINOR_SECURITYFIX</b></dt>
<dt>0x0000000f</dt>
</dl>
</td>
<td width="60%">
Security update.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_STOP_REASON_MINOR_SECURITYFIX_UNINSTALL"></a><a id="service_stop_reason_minor_securityfix_uninstall"></a><dl>
<dt><b>SERVICE_STOP_REASON_MINOR_SECURITYFIX_UNINSTALL</b></dt>
<dt>0x00000015</dt>
</dl>
</td>
<td width="60%">
Security update  uninstall.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_STOP_REASON_MINOR_SERVICEPACK"></a><a id="service_stop_reason_minor_servicepack"></a><dl>
<dt><b>SERVICE_STOP_REASON_MINOR_SERVICEPACK</b></dt>
<dt>0x0000000d</dt>
</dl>
</td>
<td width="60%">
Service pack.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_STOP_REASON_MINOR_SERVICEPACK_UNINSTALL"></a><a id="service_stop_reason_minor_servicepack_uninstall"></a><dl>
<dt><b>SERVICE_STOP_REASON_MINOR_SERVICEPACK_UNINSTALL</b></dt>
<dt>0x00000013</dt>
</dl>
</td>
<td width="60%">
Service pack uninstall.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_STOP_REASON_MINOR_SOFTWARE_UPDATE"></a><a id="service_stop_reason_minor_software_update"></a><dl>
<dt><b>SERVICE_STOP_REASON_MINOR_SOFTWARE_UPDATE</b></dt>
<dt>0x0000000e</dt>
</dl>
</td>
<td width="60%">
Software update.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_STOP_REASON_MINOR_SOFTWARE_UPDATE_UNINSTALL"></a><a id="service_stop_reason_minor_software_update_uninstall"></a><dl>
<dt><b>SERVICE_STOP_REASON_MINOR_SOFTWARE_UPDATE_UNINSTALL</b></dt>
<dt>0x0000000e</dt>
</dl>
</td>
<td width="60%">
Software update uninstall.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_STOP_REASON_MINOR_UNSTABLE"></a><a id="service_stop_reason_minor_unstable"></a><dl>
<dt><b>SERVICE_STOP_REASON_MINOR_UNSTABLE</b></dt>
<dt>0x00000007</dt>
</dl>
</td>
<td width="60%">
Unstable.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_STOP_REASON_MINOR_UPGRADE"></a><a id="service_stop_reason_minor_upgrade"></a><dl>
<dt><b>SERVICE_STOP_REASON_MINOR_UPGRADE</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Upgrade.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_STOP_REASON_MINOR_WMI"></a><a id="service_stop_reason_minor_wmi"></a><dl>
<dt><b>SERVICE_STOP_REASON_MINOR_WMI</b></dt>
<dt>0x00000012</dt>
</dl>
</td>
<td width="60%">
WMI issue.

</td>
</tr>
</table>

### -field pszComment

An optional string that provides additional information about the service stop. This string is stored in the event log along with the stop reason code. This member must be <b>NULL</b> or a valid string that is less than 128 characters, including the terminating null character.

### -field ServiceStatus

A pointer to a 
<a href="/windows/desktop/api/winsvc/ns-winsvc-service_status_process">SERVICE_STATUS_PROCESS</a> structure that receives the latest service status information. The information returned reflects the most recent status that the service reported to the service control manager. 




The service control manager fills in the structure only when 
<a href="/windows/desktop/api/winsvc/nf-winsvc-controlserviceexa">ControlServiceEx</a> returns one of the following error codes: NO_ERROR, ERROR_INVALID_SERVICE_CONTROL, ERROR_SERVICE_CANNOT_ACCEPT_CTRL, or ERROR_SERVICE_NOT_ACTIVE. Otherwise, the structure is not filled in.

## -see-also

<a href="/windows/desktop/api/winsvc/nf-winsvc-controlserviceexa">ControlServiceEx</a>



<a href="/windows/desktop/api/winsvc/ns-winsvc-service_status_process">SERVICE_STATUS_PROCESS</a>

## -remarks

> [!NOTE]
> The winsvc.h header defines SERVICE_CONTROL_STATUS_REASON_PARAMS as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
