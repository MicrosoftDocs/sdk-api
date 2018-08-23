---
UID: NF:wininet.InternetAutodial
title: InternetAutodial function
author: windows-sdk-content
description: Causes the modem to automatically dial the default Internet connection.
old-location: wininet\internetautodial.htm
old-project: WinInet
ms.assetid: 843875a8-6c83-4259-8e46-a04f786eb230
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: INTERNET_AUTODIAL_FAILIFSECURITYCHECK, INTERNET_AUTODIAL_FORCE_ONLINE, INTERNET_AUTODIAL_FORCE_UNATTENDED, INTERNET_AUTODIAL_OVERRIDE_NET_PRESENT, InternetAutodial, InternetAutodial function [WinINet], _inet_internetautodial_function, wininet.internetautodial, winineti/InternetAutodial
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wininet.h
req.include-header: Wininet.h
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
req.typenames: InternetCookieState
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wininet.dll
api_name:
 - InternetAutodial
product: Windows
targetos: Windows
req.lib: Wininet.lib
req.dll: Wininet.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# InternetAutodial function


## -description


Causes the modem to automatically dial the default Internet connection.


## -parameters




### -param dwFlags [in]

Controls this operation. This parameter can be one  of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="INTERNET_AUTODIAL_FAILIFSECURITYCHECK"></a><a id="internet_autodial_failifsecuritycheck"></a><dl>
<dt><b>INTERNET_AUTODIAL_FAILIFSECURITYCHECK</b></dt>
<dt>0x04</dt>
</dl>
</td>
<td width="60%">
Causes 
<b>InternetAutodial</b> to fail if file and printer sharing is disabled for Windows 95 or later.

<b>Windows Server 2008 and Windows Vista:  </b>This flag is  obsolete.

</td>
</tr>
<tr>
<td width="40%"><a id="INTERNET_AUTODIAL_FORCE_ONLINE"></a><a id="internet_autodial_force_online"></a><dl>
<dt><b>INTERNET_AUTODIAL_FORCE_ONLINE</b></dt>
<dt> 0x01</dt>
</dl>
</td>
<td width="60%">
Forces an online Internet connection.

</td>
</tr>
<tr>
<td width="40%"><a id="INTERNET_AUTODIAL_FORCE_UNATTENDED"></a><a id="internet_autodial_force_unattended"></a><dl>
<dt><b>INTERNET_AUTODIAL_FORCE_UNATTENDED</b></dt>
<dt> 0x02</dt>
</dl>
</td>
<td width="60%">
Forces an unattended Internet dial-up.

</td>
</tr>
<tr>
<td width="40%"><a id="INTERNET_AUTODIAL_OVERRIDE_NET_PRESENT"></a><a id="internet_autodial_override_net_present"></a><dl>
<dt><b>INTERNET_AUTODIAL_OVERRIDE_NET_PRESENT</b></dt>
<dt> 0x08</dt>
</dl>
</td>
<td width="60%">
Causes <b>InternetAutodial</b> to dial the modem connection even when a network connection to the Internet is present.

</td>
</tr>
</table>
 


### -param hwndParent [in]

Handle to the parent window.


## -returns



If the function succeeds, it returns <b>TRUE</b>.


If the function fails, it returns <b>FALSE</b>. Applications can call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> to retrieve the error code.




## -remarks



<b>InternetAutodial</b> does not support double-dial connections, SmartCard authentication, or connections that require registry-based certification.

<div class="alert"><b>Note</b>  Starting on Windows Vista and Windows Server 2008, the WinINet dial-up functions use the <a href="https://msdn.microsoft.com/5883a77a-6af8-47a8-bb28-6ef60a5aa2f1">RAS  functions</a> to establish a dial-up connection. WinINet supports the functionality documented in the <a href="https://msdn.microsoft.com/698a18a1-b302-4b0d-8399-0bbdbe775f08">RasDialDlg</a> function.</div>
<div> </div>
<b>InternetAutodial</b> does not attempt to dial if there is an existing dial-up connection on the system. Also, if there is an existing LAN connection, and <b>InternetAutodial</b> is not configured to force dial (set the <b>INTERNET_AUTODIAL_FORCE_ONLINE</b> in the <i>dwFlags</i> parameter), <b>InternetAutodial</b> does not attempt to dial the connection and returns <b>TRUE</b>.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/dd33ed4b-eb7c-449c-b309-8f5c290a5a93">Establishing a Dial-Up Connection to the Internet</a>



<a href="https://msdn.microsoft.com/2e0da5c6-29e4-47b5-8ed2-8712c9ca2c97">WinINet Functions</a>
 

 

