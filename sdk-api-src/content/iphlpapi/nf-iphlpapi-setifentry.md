---
UID: NF:iphlpapi.SetIfEntry
title: SetIfEntry function (iphlpapi.h)
description: The SetIfEntry function sets the administrative status of an interface.
helpviewer_keywords: ["MIB_IF_ADMIN_STATUS_DOWN","MIB_IF_ADMIN_STATUS_UP","SetIfEntry","SetIfEntry function [IP Helper]","_iphlp_setifentry","iphlp.setifentry","iphlpapi/SetIfEntry"]
old-location: iphlp\setifentry.htm
tech.root: IpHlp
ms.assetid: 67a18ef2-a7af-4fc1-8416-053aa8388f9e
ms.date: 12/05/2018
ms.keywords: MIB_IF_ADMIN_STATUS_DOWN, MIB_IF_ADMIN_STATUS_UP, SetIfEntry, SetIfEntry function [IP Helper], _iphlp_setifentry, iphlp.setifentry, iphlpapi/SetIfEntry
req.header: iphlpapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Iphlpapi.lib
req.dll: Iphlpapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetIfEntry
 - iphlpapi/SetIfEntry
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Iphlpapi.dll
api_name:
 - SetIfEntry
---

# SetIfEntry function


## -description

The 
<b>SetIfEntry</b> function sets the administrative status of an interface.

## -parameters

### -param pIfRow [in]

A pointer to a 
<a href="/windows/desktop/api/ifmib/ns-ifmib-mib_ifrow">MIB_IFROW</a> structure. The <b>dwIndex</b> member of this structure specifies the interface on which to set administrative status. The <b>dwAdminStatus</b> member specifies the new administrative status. The <b>dwAdminStatus</b> member can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MIB_IF_ADMIN_STATUS_UP"></a><a id="mib_if_admin_status_up"></a><dl>
<dt><b>MIB_IF_ADMIN_STATUS_UP</b></dt>
</dl>
</td>
<td width="60%">
The interface is administratively enabled.

</td>
</tr>
<tr>
<td width="40%"><a id="MIB_IF_ADMIN_STATUS_DOWN"></a><a id="mib_if_admin_status_down"></a><dl>
<dt><b>MIB_IF_ADMIN_STATUS_DOWN</b></dt>
</dl>
</td>
<td width="60%">
The interface is administratively disabled.

</td>
</tr>
</table>

## -returns

If the function succeeds, the return value is NO_ERROR.

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
Access is denied. This error is returned on Windows Vista and later under several conditions that include the following: the  user lacks the required administrative privileges on the local computer or the application is not running in an enhanced shell as the built-in Administrator (RunAs administrator).  

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The system cannot find the file specified. This error is returned on Windows Vista and later if the  network interface specified by the <b>dwIndex</b>  member of the <a href="/windows/desktop/api/ifmib/ns-ifmib-mib_ifrow">MIB_IFROW</a> structure pointed to by the <i>pIfRow</i> parameter could not be found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter was passed to the function. This error is returned if a <b>NULL</b> pointer is passed in the <i>pIfRow</i> parameter, or the <b>dwIndex</b>  member of the <a href="/windows/desktop/api/ifmib/ns-ifmib-mib_ifrow">MIB_IFROW</a> pointed to by the <i>pIfRow</i> parameter was unspecified. This error is also returned on Windows Server 2003 and earlier if the  network interface specified by the <b>dwIndex</b>  member of the <b>MIB_IFROW</b> structure pointed to by the <i>pIfRow</i> parameter could not be found.  

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The request is not supported. This error is returned on Windows Server 2003 and earlier if no TCP/IP stack is configured on the local computer.  

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Other</b></dt>
</dl>
</td>
<td width="60%">
Use 
<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> to obtain the message string for the returned error.

</td>
</tr>
</table>

## -remarks

The <b>SetIfEntry</b> function is used to set the administrative status of an interface on a local computer. 

The <b>dwIndex</b> member in the <a href="/windows/desktop/api/ifmib/ns-ifmib-mib_ifrow">MIB_IFROW</a> structure pointed to by the <i>pIfRow</i> parameter must be initialized to the interface index.


The <b>SetIfEntry</b> function will fail if the  <b>dwIndex</b>  member of the <a href="/windows/desktop/api/ifmib/ns-ifmib-mib_ifrow">MIB_IFROW</a> pointed to by the <i>pIfRow</i> parameter does not match an existing interface on the local computer. 

On Windows Vista and later, the <b>SetIfEntry</b> function can only be called by a user logged on as a member of the Administrators group. If <b>SetIfEntry</b> is called by a user that is not a member of the Administrators group, the function call will fail and <b>ERROR_ACCESS_DENIED</b> is returned. 

The <b>SetIfEntry</b> function can also fail because of user account control (UAC) on Windows Vista and later. If an application that contains this function is executed by a user logged on as a member of the Administrators group other than the built-in Administrator, this call will fail unless the application has been marked in the manifest file with a <b>requestedExecutionLevel</b> set to requireAdministrator. If the application lacks this manifest file, a user logged on as a member of the Administrators group other than the built-in Administrator must then be executing the application in an enhanced shell as the built-in Administrator (RunAs administrator) for this function to succeed.



<div class="alert"><b>Note</b>   On Windows NT 4.0 and Windows 2000 and later, this function executes a privileged operation. For this function to execute successfully, the caller must be logged on as a member of the Administrators group or the NetworkConfigurationOperators group.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getifentry">GetIfEntry</a>



<b>GetIfTable</b>



<a href="/windows/desktop/IpHlp/ip-helper-function-reference">IP Helper Function Reference</a>



<a href="/windows/desktop/IpHlp/ip-helper-start-page">IP Helper Start Page</a>



<a href="/windows/desktop/api/ifmib/ns-ifmib-mib_ifrow">MIB_IFROW</a>



<a href="/windows/desktop/api/ifmib/ns-ifmib-mib_iftable">MIB_IFTABLE</a>