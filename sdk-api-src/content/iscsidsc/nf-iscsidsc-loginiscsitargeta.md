---
UID: NF:iscsidsc.LoginIScsiTargetA
title: LoginIScsiTargetA function
author: windows-sdk-content
description: LoginIscsiTarget function establishes a full featured login session with the indicated target.
old-location: iscsidisc\loginiscsitarget.htm
old-project: iSCSIDisc
ms.assetid: e94e72d2-b93c-41f4-aafc-78e6a97d7a26
ms.author: windowssdkdev
ms.date: 06/14/2018
ms.keywords: ISCSI_SECURITY_FLAG_AGGRESSIVE_MODE_ENABLED, ISCSI_SECURITY_FLAG_IKE_IPSEC_ENABLED, ISCSI_SECURITY_FLAG_MAIN_MODE_ENABLED, ISCSI_SECURITY_FLAG_PFS_ENABLED, ISCSI_SECURITY_FLAG_TRANSPORT_MODE_PREFERRED, ISCSI_SECURITY_FLAG_TUNNEL_MODE_PREFERRED, ISCSI_SECURITY_FLAG_VALID, LoginIScsiTargetA, LoginIscsiTarget, LoginIscsiTarget function [iSCSI Discovery Library API], LoginIscsiTargetA, LoginIscsiTargetW, iscsidisc.loginiscsitarget, iscsidsc/LoginIscsiTarget, iscsidsc/LoginIscsiTargetA, iscsidsc/LoginIscsiTargetW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: iscsidsc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: LoginIscsiTargetW (Unicode) and LoginIscsiTargetA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TARGET_INFORMATION_CLASS, *PTARGET_INFORMATION_CLASS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Iscsidsc.dll
api_name:
 - LoginIscsiTarget
 - LoginIscsiTargetA
 - LoginIscsiTargetW
product: Windows
targetos: Windows
req.lib: Iscsidsc.lib
req.dll: Iscsidsc.dll
req.irql: 
req.product: GDI+ 1.1
---

# LoginIScsiTargetA function


## -description


The <b>LoginIscsiTarget</b> function establishes a full featured login session with the indicated target.


## -parameters




### -param TargetName [in]

The name of the target with which to establish a login session. The target must already exist in the list of discovered targets for the iSCSI initiator service.


### -param IsInformationalSession [in]

If <b>true</b>, the <b>LoginIscsiTarget</b> function establishes a login session, but the operation does not report the LUNs on the target to the "Plug and Play" Manager. If the login succeeds, management applications will be able to query the target for information with the <a href="https://msdn.microsoft.com/0898daf0-67ae-47a4-90bf-2112b6e6b20c">SendScsiReportLuns</a> and <a href="https://msdn.microsoft.com/1a12848f-4b2d-45f6-971b-d8e4ccd00c21">SendScsiReadCapacity</a> functions, but the storage stack will not enumerate the target or load a driver for it. 

If <i>IsInformationalSession</i> is <b>false</b>, <b>LoginIscsiTarget</b> reports the LUNs associated with the target to the "Plug and Play" Manager, and the system loads drivers for the LUNs.


### -param InitiatorInstance

TBD


### -param InitiatorPortNumber [in, optional]

The port number of the Host Bus Adapter (HBA) that initiates the login session. If this parameter is <b>ISCSI_ANY_INITIATOR_PORT</b>, the caller did not specify a port for the initiator HBA to use when logging in to the target. 

If <i>InitiatorName</i> is <b>null</b>, <i>InitiatorPortNumber</i> must be <b>ISCSI_ANY_INITIATOR_PORT</b>. 


### -param TargetPortal [in, optional]

Pointer to a structure of type <a href="https://msdn.microsoft.com/de78c7ec-c2ce-493a-ad29-2ea10e3d7dff">ISCSI_TARGET_PORTAL</a> that indicates the portal that the initiator uses to open the session. The specified portal must belong to a portal group that is associated with the <i>TargetName</i>. If <i>TargetPortal</i> is <b>null</b>, the iSCSI initiator service instructs the initiator to use any portal through which the target is accessible to the initiator. If the caller specifies the value for <i>TargetPortal</i>, the iSCSI initiator service will not verify that the <i>TargetPortal</i> is accessible to the initiator HBA.


### -param SecurityFlags [in, optional]

A bitmap that specifies the characteristics of the IPsec connection that the initiator adds to the session. If an IPsec security policy between the initiator and the target portal is already configured as a result of the current portal group policy or a previous connection to the target, the existing configuration takes precedence over the configuration specified in <i>SecurityFlags</i>. 

If the ISCSI_SECURITY_FLAG_VALID flag is set to 0, the iSCSI initiator service uses default values for the security flags that are defined in the registry. 

Caller can set any of the following flags in the bitmap: 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ISCSI_SECURITY_FLAG_TUNNEL_MODE_PREFERRED"></a><a id="iscsi_security_flag_tunnel_mode_preferred"></a><dl>
<dt><b>ISCSI_SECURITY_FLAG_TUNNEL_MODE_PREFERRED</b></dt>
</dl>
</td>
<td width="60%">
When set to 1, the initiator should make the connection in IPsec tunnel mode. Caller should set this flag or the ISCSI_SECURITY_FLAG_TRANSPORT_MODE_PREFERRED flag, but not both.

</td>
</tr>
<tr>
<td width="40%"><a id="ISCSI_SECURITY_FLAG_TRANSPORT_MODE_PREFERRED"></a><a id="iscsi_security_flag_transport_mode_preferred"></a><dl>
<dt><b>ISCSI_SECURITY_FLAG_TRANSPORT_MODE_PREFERRED</b></dt>
</dl>
</td>
<td width="60%">
When set to 1, the initiator should make the connection in IPsec transport mode. Caller should set this flag or the ISCSI_SECURITY_FLAG_TUNNEL_MODE_PREFERRED flag, but not both.

</td>
</tr>
<tr>
<td width="40%"><a id="ISCSI_SECURITY_FLAG_PFS_ENABLED"></a><a id="iscsi_security_flag_pfs_enabled"></a><dl>
<dt><b>ISCSI_SECURITY_FLAG_PFS_ENABLED</b></dt>
</dl>
</td>
<td width="60%">
When set to 1, the initiator should make the connection with Perfect Forward Secrecy (PFS) mode enabled; otherwise, the initiator should make the connection with PFS mode disabled. 

</td>
</tr>
<tr>
<td width="40%"><a id="ISCSI_SECURITY_FLAG_AGGRESSIVE_MODE_ENABLED"></a><a id="iscsi_security_flag_aggressive_mode_enabled"></a><dl>
<dt><b>ISCSI_SECURITY_FLAG_AGGRESSIVE_MODE_ENABLED</b></dt>
</dl>
</td>
<td width="60%">
When set to 1, the initiator should make the connection with aggressive mode enabled. Caller should set this flag or the ISCSI_SECURITY_FLAG_MAIN_MODE_ENABLED flag, but not both. 



<div class="alert"><b>Note</b>  The Microsoft software initiator driver does not support aggressive mode.
</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="ISCSI_SECURITY_FLAG_MAIN_MODE_ENABLED"></a><a id="iscsi_security_flag_main_mode_enabled"></a><dl>
<dt><b>ISCSI_SECURITY_FLAG_MAIN_MODE_ENABLED</b></dt>
</dl>
</td>
<td width="60%">
When set to 1, the initiator should make the connection with main mode enabled. Caller should set this flag or the ISCSI_SECURITY_FLAG_AGGRESSIVE_MODE_ENABLED flag, but not both.

</td>
</tr>
<tr>
<td width="40%"><a id="ISCSI_SECURITY_FLAG_IKE_IPSEC_ENABLED"></a><a id="iscsi_security_flag_ike_ipsec_enabled"></a><dl>
<dt><b>ISCSI_SECURITY_FLAG_IKE_IPSEC_ENABLED</b></dt>
</dl>
</td>
<td width="60%">
When set to 1, the initiator should make the connection with the IKE/IPsec protocol enabled; otherwise, the IKE/IPsec protocol is disabled.

</td>
</tr>
<tr>
<td width="40%"><a id="ISCSI_SECURITY_FLAG_VALID"></a><a id="iscsi_security_flag_valid"></a><dl>
<dt><b>ISCSI_SECURITY_FLAG_VALID</b></dt>
</dl>
</td>
<td width="60%">
When set to 1, the other mask values are valid; otherwise, the iSCSI initiator service will use bitmap values that were previously defined for the target portal, or if none are available, the initiator service uses the default values defined in the registry. 

</td>
</tr>
</table>
 


### -param Mappings [in, optional]

An array of structures of type <a href="https://msdn.microsoft.com/bdc27e67-1d64-42cd-adfa-a792012b7142">ISCSI_TARGET_MAPPING</a>, each of which holds information that the initiator uses to assign bus, target and LUN numbers to the devices that are associated with the target. If <i>Mappings</i> is <b>null</b>, the initiator will select the bus, target and LUN numbers.


### -param LoginOptions [in, optional]

A pointer to a structure of type <a href="https://msdn.microsoft.com/7d45be86-3d85-4253-aef7-92e05379f1b2">ISCSI_LOGIN_OPTIONS</a> that contains the options that specify the characteristics of the login session.


### -param KeySize [in, optional]

The size, in bytes, of the target's preshared key specified by the <i>Key</i> parameter.


### -param Key [in, optional]

A preshared key to use when logging in to the target portal that exposes this target. 

<div class="alert"><b>Note</b>  If an IPsec policy is already associated with the target portal, the IPsec settings in this call are ignored.</div>
<div> </div>

### -param IsPersistent [in]

If <b>true</b>, the initiator should save the characteristics of the login session in non-volatile storage, so that the information persists across restarts of the initiator device and reboots of the operating system. The initiator should not establish the login session until after saving the persistent data. 

Whenever the initiator device restarts, it should automatically attempt to re-establish the login session with the same characteristics. If <b>false</b>, the initiator device simply logs in to the target without saving the characteristics of the login session.


### -param UniqueSessionId [out]

A pointer to a structure of type <a href="https://msdn.microsoft.com/d13975f9-58d0-425c-a2de-a0d1d70850d3">ISCSI_UNIQUE_SESSION_ID</a> that, on return, contains a unique session identifier for the login session. 



### -param UniqueConnectionId [out]

A pointer to a structure of type <a href="https://msdn.microsoft.com/cc68fda4-6dbf-42de-8e0e-e144bd4e9524">ISCSI_UNIQUE_CONNECTION_ID</a> that, on return, contains a unique connection identifier for the login session. 



#### - InitiatorName [in, optional]

The name of the initiator that logs in to the target. If <i>InitiatorName</i> is <b>null</b>, the iSCSI initiator service selects an initiator. 


## -returns



Returns ERROR_SUCCESS if the operation succeeds. Otherwise, it returns the appropriate Win32 or iSCSI error code.





## -remarks



The <b>LoginIscsiTarget</b> function either establishes a single login session with a target, or creates a persistent login to a target. If <b>LoginIscsiTarget</b> creates a persistent login, the specified initiator should log in to the target each time the initiator is started, typically at system boot. Callers to <b>LoginIscsiTarget</b> can request the creation of a persistent login by setting the <i>IsPersistent</i> parameter to <b>true</b>.




## -see-also




<a href="https://msdn.microsoft.com/7d45be86-3d85-4253-aef7-92e05379f1b2">ISCSI_LOGIN_OPTIONS</a>



<a href="https://msdn.microsoft.com/de78c7ec-c2ce-493a-ad29-2ea10e3d7dff">ISCSI_TARGET_PORTAL</a>



<a href="https://msdn.microsoft.com/cc68fda4-6dbf-42de-8e0e-e144bd4e9524">ISCSI_UNIQUE_CONNECTION_ID</a>



<a href="https://msdn.microsoft.com/d13975f9-58d0-425c-a2de-a0d1d70850d3">ISCSI_UNIQUE_SESSION_ID</a>
 

 

