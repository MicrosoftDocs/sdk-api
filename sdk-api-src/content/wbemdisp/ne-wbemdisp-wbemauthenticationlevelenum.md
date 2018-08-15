---
UID: NE:wbemdisp.WbemAuthenticationLevelEnum
title: WbemAuthenticationLevelEnum
author: windows-sdk-content
description: Define the security authentication levels.
old-location: wmi\wbemauthenticationlevelenum.htm
old-project: WmiSdk
ms.assetid: 1789b25a-e9a0-42a3-97c2-077e902a2f41
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: WbemAuthenticationLevelCall, WbemAuthenticationLevelConnect, WbemAuthenticationLevelDefault, WbemAuthenticationLevelEnum, WbemAuthenticationLevelEnum enumeration [Windows Management Instrumentation], WbemAuthenticationLevelNone, WbemAuthenticationLevelPkt, WbemAuthenticationLevelPktIntegrity, WbemAuthenticationLevelPktPrivacy, _hmm_wbemauthenticationlevelenum, wbemdisp/WbemAuthenticationLevelCall, wbemdisp/WbemAuthenticationLevelConnect, wbemdisp/WbemAuthenticationLevelDefault, wbemdisp/WbemAuthenticationLevelEnum, wbemdisp/WbemAuthenticationLevelNone, wbemdisp/WbemAuthenticationLevelPkt, wbemdisp/WbemAuthenticationLevelPktIntegrity, wbemdisp/WbemAuthenticationLevelPktPrivacy, wmi.wbemauthenticationlevelenum
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: wbemdisp.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wbemdisp.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WbemAuthenticationLevelEnum
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wbemdisp.h
api_name:
 - WbemAuthenticationLevelEnum
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# WbemAuthenticationLevelEnum enumeration


## -description


The 
<b>WbemAuthenticationLevelEnum</b> constants define the security authentication levels. These constants are used with 
<a href="https://msdn.microsoft.com/794587fa-5feb-455b-be28-ecfaa25625ad">SWbemSecurity</a> and in moniker connections to WMI.

The WMI scripting type library, wbemdisp.tlb, defines these constants. Visual Basic applications can access this library.

Script languages must use one of the following:
<ul>
<li>
The short name. For example, for <b>WbemAuthenticationLevelPktPrivacy</b> use "PktPrivacy".

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>
strComputer = "RemoteComputer"
Set objWMIServices = GetObject("WINMGMTS:" _
    &amp; "{authenticationLevel=pktPrivacy}!\\" _
    &amp; strComputer &amp; "\ROOT\CIMV2")</pre>
</td>
</tr>
</table></span></div>
</li>
<li>
Windows Script Host (WSH) XML file format in the script. For example, this means that the script can use the  <b>WbemAuthenticationLevelPkt</b> constant directly.

The following WSH script sets the authentication level. To run the script, save the text in a file with a .wsf extension.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>&lt;?xml version="1.0" encoding="US-ASCII"?&gt;
&lt;job&gt;
&lt;reference object="WbemScripting.SWbemLocator"/&gt;
&lt;script language="VBScript"&gt;
    set service = GetObject("winmgmts:")
    ' Following line uses a symbolic 
    ' constant from the WMI type library
    service.Security_.authenticationLevel = _
        WbemAuthenticationLevelPktPrivacy
&lt;/script&gt;
&lt;/job&gt;
</pre>
</td>
</tr>
</table></span></div>For more information, see 
<a href="https://msdn.microsoft.com/6ef4e210-0733-4f2a-89c1-1a7aca5a19d9">Using the WMI Scripting Type Library</a>.</li>
</ul>

## -enum-fields




### -field wbemAuthenticationLevelDefault


### -field wbemAuthenticationLevelNone


### -field wbemAuthenticationLevelConnect


### -field wbemAuthenticationLevelCall


### -field wbemAuthenticationLevelPkt


### -field wbemAuthenticationLevelPktIntegrity


### -field wbemAuthenticationLevelPktPrivacy




#### - WbemAuthenticationLevelCall

Short name: Call

Authenticates only at the beginning of each call when the server receives the request.


#### - WbemAuthenticationLevelConnect

Short name: Connect

Authenticates the credentials of the client only when the client establishes a relationship with the server.


#### - WbemAuthenticationLevelDefault

Short name: Default

WMI uses the default Windows Authentication setting.


#### - WbemAuthenticationLevelNone

Short name: None

Uses no authentication.


#### - WbemAuthenticationLevelPkt

Short name: Pkt

Authenticates that all data received is from the expected client.


#### - WbemAuthenticationLevelPktIntegrity

Short name: PktIntegrity

Authenticates and verifies that none of the data transferred between client and server has been modified.


#### - WbemAuthenticationLevelPktPrivacy

Short name: PktPrivacy

Authenticates all previous impersonation levels and encrypts the argument value of each remote procedure call.


## -see-also




<a href="https://msdn.microsoft.com/1aacc523-2a2f-43f5-96a3-aa0387cbae3e">Constructing a Moniker String</a>



<a href="https://msdn.microsoft.com/794587fa-5feb-455b-be28-ecfaa25625ad">SWbemSecurity</a>



<a href="https://msdn.microsoft.com/feaab757-3167-420b-8f42-edced4cd4c53">Scripting API Constants</a>



<a href="https://msdn.microsoft.com/f665fc60-68bd-495d-a441-e3a9473f9d89">Setting Security on an Asynchronous Call in VBScript</a>



<a href="https://msdn.microsoft.com/cb477224-3117-45e4-9271-613b58e48b6e">Setting the Default Process Security Level Using VBScript</a>
 

 

