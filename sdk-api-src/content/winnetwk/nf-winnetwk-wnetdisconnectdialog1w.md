---
UID: NF:winnetwk.WNetDisconnectDialog1W
title: WNetDisconnectDialog1W function
author: windows-sdk-content
description: The WNetDisconnectDialog1 function attempts to disconnect a network resource.
old-location: wnet\wnetdisconnectdialog1.htm
tech.root: WNet
ms.assetid: ec3abf0c-2a18-4d7d-aac4-e086d00fa6fe
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: WNetDisconnectDialog1, WNetDisconnectDialog1 function [Windows Networking (WNet)], WNetDisconnectDialog1A, WNetDisconnectDialog1W, _win32_wnetdisconnectdialog1, winnetwk/WNetDisconnectDialog1, winnetwk/WNetDisconnectDialog1A, winnetwk/WNetDisconnectDialog1W, wnet.wnetdisconnectdialog1
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
req.unicode-ansi: WNetDisconnectDialog1W (Unicode) and WNetDisconnectDialog1A (ANSI)
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
 - WNetDisconnectDialog1
 - WNetDisconnectDialog1A
 - WNetDisconnectDialog1W
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WNetDisconnectDialog1W function


## -description


The
				<b>WNetDisconnectDialog1</b> function attempts to disconnect a network resource. If the underlying network returns ERROR_OPEN_FILES, the function prompts the user for confirmation. If there is any error, the function informs the user. The function requires a 
<a href="https://msdn.microsoft.com/ae415815-f247-4217-a4f1-6a7ca9288890">DISCDLGSTRUCT</a> to specify the parameters for the disconnect attempt.


## -parameters




### -param lpConnDlgStruct [in]

Pointer to a 
<b>DISCDLGSTRUCT</b> structure. The structure specifies the behavior for the disconnect attempt.


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
<dt><b>ERROR_CANCELLED</b></dt>
</dl>
</td>
<td width="60%">
When the system prompted the user for a decision about disconnecting, the user elected not to disconnect.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_OPEN_FILES</b></dt>
</dl>
</td>
<td width="60%">
Unable to disconnect because the user is actively using the connection.

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
There is insufficient memory to start the dialog box.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_EXTENDED_ERROR</b></dt>
</dl>
</td>
<td width="60%">
A network-specific error occurred. Call the 
<a href="https://msdn.microsoft.com/8e13c467-adcf-4e97-b51a-1f5fc919b51e">WNetGetLastError</a> function to obtain a description of the error.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/ae415815-f247-4217-a4f1-6a7ca9288890">DISCDLGSTRUCT</a>



<a href="https://msdn.microsoft.com/2dc383bb-0a1a-4612-88f9-f92c8e2a398d">WNetConnectionDialog</a>



<a href="https://msdn.microsoft.com/11390693-0ab3-4f8b-9209-bc0bceb98032">WNetConnectionDialog1</a>



<a href="https://msdn.microsoft.com/76e0f38a-e057-4496-9c2f-7ea73d19bd76">WNetDisconnectDialog</a>



<a href="https://msdn.microsoft.com/7668ac55-7104-4ddb-88eb-920cfe4e36fd">Windows
		  Networking (WNet) Overview</a>



<a href="https://msdn.microsoft.com/95e30f8f-a326-424d-bd80-5fc9b3078dad">Windows
		  Networking Functions</a>
 

 

