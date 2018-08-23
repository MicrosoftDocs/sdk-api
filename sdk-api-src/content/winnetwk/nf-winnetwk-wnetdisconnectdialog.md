---
UID: NF:winnetwk.WNetDisconnectDialog
title: WNetDisconnectDialog function
author: windows-sdk-content
description: The WNetDisconnectDialog function starts a general browsing dialog box for disconnecting from network resources. The function requires a handle to the owner window for the dialog box.
old-location: wnet\wnetdisconnectdialog.htm
old-project: wnet
ms.assetid: 76e0f38a-e057-4496-9c2f-7ea73d19bd76
ms.author: windowssdkdev
ms.date: 08/17/2018
ms.keywords: RESOURCETYPE_DISK, WNetDisconnectDialog, WNetDisconnectDialog function [Windows Networking (WNet)], _win32_wnetdisconnectdialog, winnetwk/WNetDisconnectDialog, wnet.wnetdisconnectdialog
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winnetwk.h
req.include-header: 
req.redist: 
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
 - WNetDisconnectDialog
product: Windows
targetos: Windows
req.lib: Mpr.lib
req.dll: Mpr.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WNetDisconnectDialog function


## -description


The
				<b>WNetDisconnectDialog</b> function starts a general browsing dialog box for disconnecting from network resources. The function requires a handle to the owner window for the dialog box.


## -parameters




### -param hwnd [in]

Handle to the owner window for the dialog box.


### -param dwType [in]

Resource type to disconnect from. This parameter can have the following value. 



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
Disconnects from disk resources.

</td>
</tr>
</table>
 


## -returns



If the function succeeds, the return value is NO_ERROR. If the user cancels the dialog box, the return value is –1.

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



The 
<b>WNetDisconnectDialog</b> function returns immediately and creates a dialog box for disconnecting networked drives. This dialog box runs asynchronously on a worker thread.

If the worker thread is terminated, the owner window and its associated dialog box are also terminated. If this occurs, the user might not be able to interact with the dialog box, because it will not  appear on the user's screen or will appear briefly.




## -see-also




<a href="https://msdn.microsoft.com/faec728c-f19e-418c-9bdb-cde93e7d98fb">WNetAddConnection2</a>



<a href="https://msdn.microsoft.com/8bb8222f-6ede-4bf4-a6e4-681560cce162">WNetCancelConnection2</a>



<a href="https://msdn.microsoft.com/2dc383bb-0a1a-4612-88f9-f92c8e2a398d">WNetConnectionDialog</a>



<a href="https://msdn.microsoft.com/11390693-0ab3-4f8b-9209-bc0bceb98032">WNetConnectionDialog1</a>



<a href="https://msdn.microsoft.com/7668ac55-7104-4ddb-88eb-920cfe4e36fd">Windows
		  Networking (WNet) Overview</a>



<a href="https://msdn.microsoft.com/95e30f8f-a326-424d-bd80-5fc9b3078dad">Windows
		  Networking Functions</a>
 

 

