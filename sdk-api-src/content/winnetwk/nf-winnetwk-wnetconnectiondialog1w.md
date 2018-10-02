---
UID: NF:winnetwk.WNetConnectionDialog1W
title: WNetConnectionDialog1W function
author: windows-sdk-content
description: The WNetConnectionDialog1 function brings up a general browsing dialog for connecting to network resources. The function requires a CONNECTDLGSTRUCT to establish the dialog box parameters.
old-location: wnet\wnetconnectiondialog1.htm
tech.root: WNet
ms.assetid: 11390693-0ab3-4f8b-9209-bc0bceb98032
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: WNetConnectionDialog1, WNetConnectionDialog1 function [Windows Networking (WNet)], WNetConnectionDialog1A, WNetConnectionDialog1W, _win32_wnetconnectiondialog1, winnetwk/WNetConnectionDialog1, winnetwk/WNetConnectionDialog1A, winnetwk/WNetConnectionDialog1W, wnet.wnetconnectiondialog1
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winnetwk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WNetConnectionDialog1W (Unicode) and WNetConnectionDialog1A (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mpr.lib
req.dll: Mpr.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Mpr.dll
 - API-MS-Win-Core-multipleproviderrouter-l1-1-0.dll
api_name:
 - WNetConnectionDialog1
 - WNetConnectionDialog1A
 - WNetConnectionDialog1W
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WNetConnectionDialog1W function


## -description


The
				<b>WNetConnectionDialog1</b> function brings up a general browsing dialog for connecting to network resources. The function requires a 
<a href="https://msdn.microsoft.com/fb2a4b5a-ad8a-4ebf-8430-349d821eee20">CONNECTDLGSTRUCT</a> to establish the dialog box parameters.


## -parameters




### -param lpConnDlgStruct [in, out]

Pointer to a 
<b>CONNECTDLGSTRUCT</b> structure. The structure establishes the browsing dialog parameters.


## -returns



If the user cancels the dialog box, the function returns –1. If the function is successful, it returns NO_ERROR. Also, if the call is successful, the <b>dwDevNum</b> member of the 
<b>CONNECTDLGSTRUCT</b> structure contains the number of the connected device.

Typically this dialog returns an error only if the user cannot enter a dialog session. This is because errors that occur after a dialog session are reported to the user directly. If the function fails, the return value is a 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>, such as one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
Both the CONNDLG_RO_PATH and the CONNDLG_USE_MRU dialog box options are set. (Dialog box options are specified by the <b>dwFlags</b> member of the 
<a href="https://msdn.microsoft.com/fb2a4b5a-ad8a-4ebf-8430-349d821eee20">CONNECTDLGSTRUCT</a> structure.) 




-or-

Both the CONNDLG_PERSIST and the CONNDLG_NOT_PERSIST dialog box options are set.

-or-

The CONNDLG_RO_PATH dialog box option is set and the <b>lpRemoteName</b> member of the 
<a href="https://msdn.microsoft.com/c53d078e-188a-4371-bdb9-fc023bc0c1ba">NETRESOURCE</a> structure does not point to a remote network. (The 
<b>CONNECTDLGSTRUCT</b> structure points to a 
<b>NETRESOURCE</b> structure.)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BAD_DEV_TYPE</b></dt>
</dl>
</td>
<td width="60%">
The <b>dwType</b> member of the 
<b>NETRESOURCE</b> structure is not set to RESOURCETYPE_DISK.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BUSY</b></dt>
</dl>
</td>
<td width="60%">
The network provider is busy (possibly initializing). The caller should retry.

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
There is insufficient memory to display the dialog box.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_EXTENDED_ERROR</b></dt>
</dl>
</td>
<td width="60%">
A network-specific error occurred. Call 
<a href="https://msdn.microsoft.com/8e13c467-adcf-4e97-b51a-1f5fc919b51e">WNetGetLastError</a> to obtain a description of the error.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/fb2a4b5a-ad8a-4ebf-8430-349d821eee20">CONNECTDLGSTRUCT</a>



<a href="https://msdn.microsoft.com/c53d078e-188a-4371-bdb9-fc023bc0c1ba">NETRESOURCE</a>



<a href="https://msdn.microsoft.com/2dc383bb-0a1a-4612-88f9-f92c8e2a398d">WNetConnectionDialog</a>



<a href="https://msdn.microsoft.com/76e0f38a-e057-4496-9c2f-7ea73d19bd76">WNetDisconnectDialog</a>



<a href="https://msdn.microsoft.com/7668ac55-7104-4ddb-88eb-920cfe4e36fd">Windows
		  Networking (WNet) Overview</a>



<a href="https://msdn.microsoft.com/95e30f8f-a326-424d-bd80-5fc9b3078dad">Windows
		  Networking Functions</a>
 

 

