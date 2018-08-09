---
UID: NF:iscsidsc.AddIScsiConnectionW
title: AddIScsiConnectionW function
author: windows-sdk-content
description: AddIscsiConnection function adds a new iSCSI connection to an existing session.
old-location: iscsidisc\addiscsiconnection.htm
old-project: iSCSIDisc
ms.assetid: 919bf77f-f8e5-4fd2-926d-6fbca60b2fb2
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: AddIScsiConnectionW, AddIscsiConnection, AddIscsiConnection function [iSCSI Discovery Library API], AddIscsiConnectionA, AddIscsiConnectionW, ISCSI_SECURITY_FLAG_AGGRESSIVE_MODE_ENABLED, ISCSI_SECURITY_FLAG_IKE_IPSEC_ENABLED, ISCSI_SECURITY_FLAG_MAIN_MODE_ENABLED, ISCSI_SECURITY_FLAG_PFS_ENABLED, ISCSI_SECURITY_FLAG_TRANSPORT_MODE_PREFERRED, ISCSI_SECURITY_FLAG_TUNNEL_MODE_PREFERRED, ISCSI_SECURITY_FLAG_VALID, iscsidisc.addiscsiconnection, iscsidsc/AddIscsiConnection, iscsidsc/AddIscsiConnectionA, iscsidsc/AddIscsiConnectionW
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
req.unicode-ansi: AddIscsiConnectionW (Unicode) and AddIscsiConnectionA (ANSI)
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
 - AddIscsiConnection
 - AddIscsiConnectionA
 - AddIscsiConnectionW
product: Windows
targetos: Windows
req.lib: Iscsidsc.lib
req.dll: Iscsidsc.dll
req.irql: 
req.product: GDI+ 1.1
---

# AddIScsiConnectionW function


## -description


The <b>AddIscsiConnection</b> function adds a new iSCSI connection to an existing session.


## -parameters




### -param UniqueSessionId [in]

A pointer to a structure of type <a href="https://msdn.microsoft.com/d13975f9-58d0-425c-a2de-a0d1d70850d3">ISCSI_UNIQUE_SESSION_ID</a> that, on input, contains the session identifier for the session that was added.


### -param Reserved [in]

This member should be <b>null</b> on input. 


### -param InitiatorPortNumber [in, optional]

The number of the port on the initiator that the initiator uses to add the connection. A value of <b>ISCSI_ANY_INITIATOR_PORT</b> indicates that the initiator can use any of its ports to add the connection.


### -param TargetPortal [in]

A pointer to an ISCSI_TARGET_PORTAL-type structure that indicates the target portal to use when adding the connection. 

The portal must belong to the same portal group that the initiator used to login to the target, and it must be a portal that the initiator discovered. The iSCSI initiator service does not verify that the target portal meets these requirements.


### -param SecurityFlags [in, optional]

A bitmap that specifies the characteristics of the IPsec connection that the initiator uses to establish the connection. If IPsec security policy between the initiator and the target portal is already configured because of the portal group policy or a previous connection to the portal, the existing configuration takes precedence over the configuration specified in SecurityFlags and the security bitmap is ignored. 

If the <b>ISCSI_SECURITY_FLAG_VALID</b> flag is set to 0, the iSCSI initiator service uses default values for the security flags that are defined in the registry.

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
 


### -param LoginOptions [in, optional]

A pointer to a structure of type <a href="https://msdn.microsoft.com/7d45be86-3d85-4253-aef7-92e05379f1b2">ISCSI_LOGIN_OPTIONS</a> that contains the options that specify the characteristics of the login session.


### -param KeySize [in, optional]

The size, in bytes, of the preshared key that is passed to the target. 


### -param Key [in, optional]

If the IPsec security policy between the initiator and the target portal is already configured as a result of the portal group policy or a previous connection to the portal, the existing key takes precedence over the key currently specified in this member. 


### -param ConnectionId [out, optional]

An <a href="https://msdn.microsoft.com/cc68fda4-6dbf-42de-8e0e-e144bd4e9524">ISCSI_UNIQUE_CONNECTION_ID</a>-type structure that, on output, receives an opaque value that uniquely identifies the connection that was added to the session.


## -returns



Returns ERROR_SUCCESS if the operation succeeds. Otherwise, it returns the appropriate Win32 or iSCSI error code.






## -see-also




<a href="https://msdn.microsoft.com/7d45be86-3d85-4253-aef7-92e05379f1b2">ISCSI_LOGIN_OPTIONS</a>



<a href="https://msdn.microsoft.com/de78c7ec-c2ce-493a-ad29-2ea10e3d7dff">ISCSI_TARGET_PORTAL</a>



<a href="https://msdn.microsoft.com/d13975f9-58d0-425c-a2de-a0d1d70850d3">ISCSI_UNIQUE_SESSION_ID</a>
 

 

