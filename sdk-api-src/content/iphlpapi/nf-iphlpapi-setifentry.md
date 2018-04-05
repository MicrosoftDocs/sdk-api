---
UID: NF:iphlpapi.SetIfEntry
title: SetIfEntry function
author: windows-driver-content
description: The SetIfEntry function sets the administrative status of an interface.
old-location: iphlp\setifentry.htm
old-project: IpHlp
ms.assetid: 67a18ef2-a7af-4fc1-8416-053aa8388f9e
ms.author: windowsdriverdev
ms.date: 3/19/2018
ms.keywords: MIB_IF_ADMIN_STATUS_DOWN, MIB_IF_ADMIN_STATUS_UP, SetIfEntry, SetIfEntry function [IP Helper], _iphlp_setifentry, iphlp.setifentry, iphlpapi/SetIfEntry
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: NET_ADDRESS_FORMAT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Iphlpapi.dll
api_name:
-	SetIfEntry
product: Windows
targetos: Windows
req.lib: Iphlpapi.lib
req.dll: Iphlpapi.dll
req.irql: 
req.product: GDI+ 1.1
---

# SetIfEntry function


## -description


The 
<b>SetIfEntry</b> function sets the administrative status of an interface.


## -parameters




### -param pIfRow [in]

A pointer to a 
<a href="https://msdn.microsoft.com/b08631e9-6036-4377-b2f2-4ea899acb787">MIB_IFROW</a> structure. The <b>dwIndex</b> member of this structure specifies the interface on which to set administrative status. The <b>dwAdminStatus</b> member specifies the new administrative status. The <b>dwAdminStatus</b> member can be one of the following values. 



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
The system cannot find the file specified. This error is returned on Windows Vista and later if the  network interface specified by the <b>dwIndex</b>  member of the <a href="https://msdn.microsoft.com/b08631e9-6036-4377-b2f2-4ea899acb787">MIB_IFROW</a> structure pointed to by the <i>pIfRow</i> parameter could not be found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter was passed to the function. This error is returned if a <b>NULL</b> pointer is passed in the <i>pIfRow</i> parameter, or the <b>dwIndex</b>  member of the <a href="https://msdn.microsoft.com/b08631e9-6036-4377-b2f2-4ea899acb787">MIB_IFROW</a> pointed to by the <i>pIfRow</i> parameter was unspecified. This error is also returned on Windows Server 2003 and earlier if the  network interface specified by the <b>dwIndex</b>  member of the <b>MIB_IFROW</b> structure pointed to by the <i>pIfRow</i> parameter could not be found.  

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
<a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> to obtain the message string for the returned error.

</td>
</tr>
</table>
 




## -remarks



The <b>SetIfEntry</b> function is used to set the administrative status of an interface on a local computer. 

The <b>dwIndex</b> member in the <a href="https://msdn.microsoft.com/b08631e9-6036-4377-b2f2-4ea899acb787">MIB_IFROW</a> structure pointed to by the <i>pIfRow</i> parameter must be initialized to the interface index.


The <b>SetIfEntry</b> function will fail if the  <b>dwIndex</b>  member of the <a href="https://msdn.microsoft.com/b08631e9-6036-4377-b2f2-4ea899acb787">MIB_IFROW</a> pointed to by the <i>pIfRow</i> parameter does not match an existing interface on the local computer. 

On Windows Vista and later, the <b>SetIfEntry</b> function can only be called by a user logged on as a member of the Administrators group. If <b>SetIfEntry</b> is called by a user that is not a member of the Administrators group, the function call will fail and <b>ERROR_ACCESS_DENIED</b> is returned. 

The <b>SetIfEntry</b> function can also fail because of user account control (UAC) on Windows Vista and later. If an application that contains this function is executed by a user logged on as a member of the Administrators group other than the built-in Administrator, this call will fail unless the application has been marked in the manifest file with a <b>requestedExecutionLevel</b> set to requireAdministrator. If the application lacks this manifest file, a user logged on as a member of the Administrators group other than the built-in Administrator must then be executing the application in an enhanced shell as the built-in Administrator (RunAs administrator) for this function to succeed.



<div class="alert"><b>Note</b>   On Windows NT 4.0 and Windows 2000 and later, this function executes a privileged operation. For this function to execute successfully, the caller must be logged on as a member of the Administrators group or the NetworkConfigurationOperators group.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/bf16588d-3756-469e-afa2-e2e3dd537047">GetIfEntry</a>



<b>GetIfTable</b>



<a href="https://msdn.microsoft.com/2de88e92-5fa5-4d8d-9448-67a33bf02f05">IP Helper Function Reference</a>



<a href="https://msdn.microsoft.com/4896a9f8-0486-4380-bf49-d1c9ef114acc">IP Helper Start Page</a>



<a href="https://msdn.microsoft.com/b08631e9-6036-4377-b2f2-4ea899acb787">MIB_IFROW</a>



<a href="https://msdn.microsoft.com/7c3ca3d0-b6fe-4e1c-858f-82ffb26622e7">MIB_IFTABLE</a>
 

 

