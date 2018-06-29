---
UID: NF:winnetwk.WNetConnectionDialog
title: WNetConnectionDialog function
author: windows-sdk-content
description: The WNetConnectionDialog function starts a general browsing dialog box for connecting to network resources. The function requires a handle to the owner window for the dialog box.
old-location: wnet\wnetconnectiondialog.htm
old-project: WNet
ms.assetid: 2dc383bb-0a1a-4612-88f9-f92c8e2a398d
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: RESOURCETYPE_DISK, WNetConnectionDialog, WNetConnectionDialog function [Windows Networking (WNet)], _win32_wnetconnectiondialog, winnetwk/WNetConnectionDialog, wnet.wnetconnectiondialog
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winnetwk.h
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
tech.root: 
req.typenames: WINML_VARIABLE_DESC
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Mpr.dll
 - API-MS-Win-Core-multipleproviderrouter-l1-1-0.dll
api_name:
 - WNetConnectionDialog
product: Windows
targetos: Windows
req.lib: Mpr.lib
req.dll: Mpr.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WNetConnectionDialog function


## -description


The
				<b>WNetConnectionDialog</b> function starts a general browsing dialog box for connecting to network resources. The function requires a handle to the owner window for the dialog box.


## -parameters




### -param hwnd [in]

Handle to the owner window for the dialog box.


### -param dwType [in]

Resource type to allow connections to. This parameter can be the following value. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RESOURCETYPE_DISK"></a><a id="resourcetype_disk"></a><dl>
<dt><b>RESOURCETYPE_DISK</b></dt>
</dl>
</td>
<td width="60%">
Connections to disk resources.

</td>
</tr>
</table>
 


## -returns



If the function succeeds, the return value is NO_ERROR. If the user cancels the dialog box, the function returns –1.

If the function fails, the return value is a 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>, such as one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_EXTENDED_ERROR</b></dt>
</dl>
</td>
<td width="60%">
A network-specific error occurred. To obtain a description of the error, call the 
<a href="https://msdn.microsoft.com/8e13c467-adcf-4e97-b51a-1f5fc919b51e">WNetGetLastError</a> function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PASSWORD</b></dt>
</dl>
</td>
<td width="60%">
The specified password is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_NETWORK</b></dt>
</dl>
</td>
<td width="60%">
The network is unavailable.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is insufficient memory to start the dialog box.

</td>
</tr>
</table>
 




## -remarks



If the user clicks <b>OK</b> in the dialog box, the requested network connection will have been made when the 
<b>WNetConnectionDialog</b> function returns.

If the function attempts to make a connection and the network provider returns the message ERROR_INVALID_PASSWORD, the system prompts the user to enter a password. The system uses the new password in another attempt to make the connection.




## -see-also




<a href="https://msdn.microsoft.com/169c7bb4-cb08-424c-af79-2133684a99db">WNetAddConnection3</a>



<a href="https://msdn.microsoft.com/8bb8222f-6ede-4bf4-a6e4-681560cce162">WNetCancelConnection2</a>



<a href="https://msdn.microsoft.com/76e0f38a-e057-4496-9c2f-7ea73d19bd76">WNetDisconnectDialog</a>



<a href="https://msdn.microsoft.com/7668ac55-7104-4ddb-88eb-920cfe4e36fd">Windows
		  Networking (WNet) Overview</a>



<a href="https://msdn.microsoft.com/95e30f8f-a326-424d-bd80-5fc9b3078dad">Windows
		  Networking Functions</a>
 

 

