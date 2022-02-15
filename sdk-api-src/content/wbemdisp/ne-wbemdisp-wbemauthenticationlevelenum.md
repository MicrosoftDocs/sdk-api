---
UID: NE:wbemdisp.WbemAuthenticationLevelEnum
title: WbemAuthenticationLevelEnum (wbemdisp.h)
description: Define the security authentication levels.
helpviewer_keywords: ["WbemAuthenticationLevelCall","WbemAuthenticationLevelConnect","WbemAuthenticationLevelDefault","WbemAuthenticationLevelEnum","WbemAuthenticationLevelEnum enumeration [Windows Management Instrumentation]","WbemAuthenticationLevelNone","WbemAuthenticationLevelPkt","WbemAuthenticationLevelPktIntegrity","WbemAuthenticationLevelPktPrivacy","_hmm_wbemauthenticationlevelenum","wbemdisp/WbemAuthenticationLevelCall","wbemdisp/WbemAuthenticationLevelConnect","wbemdisp/WbemAuthenticationLevelDefault","wbemdisp/WbemAuthenticationLevelEnum","wbemdisp/WbemAuthenticationLevelNone","wbemdisp/WbemAuthenticationLevelPkt","wbemdisp/WbemAuthenticationLevelPktIntegrity","wbemdisp/WbemAuthenticationLevelPktPrivacy","wmi.wbemauthenticationlevelenum"]
old-location: wmi\wbemauthenticationlevelenum.htm
tech.root: wmi
ms.assetid: 1789b25a-e9a0-42a3-97c2-077e902a2f41
ms.date: 12/05/2018
ms.keywords: WbemAuthenticationLevelCall, WbemAuthenticationLevelConnect, WbemAuthenticationLevelDefault, WbemAuthenticationLevelEnum, WbemAuthenticationLevelEnum enumeration [Windows Management Instrumentation], WbemAuthenticationLevelNone, WbemAuthenticationLevelPkt, WbemAuthenticationLevelPktIntegrity, WbemAuthenticationLevelPktPrivacy, _hmm_wbemauthenticationlevelenum, wbemdisp/WbemAuthenticationLevelCall, wbemdisp/WbemAuthenticationLevelConnect, wbemdisp/WbemAuthenticationLevelDefault, wbemdisp/WbemAuthenticationLevelEnum, wbemdisp/WbemAuthenticationLevelNone, wbemdisp/WbemAuthenticationLevelPkt, wbemdisp/WbemAuthenticationLevelPktIntegrity, wbemdisp/WbemAuthenticationLevelPktPrivacy, wmi.wbemauthenticationlevelenum
req.header: wbemdisp.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WbemAuthenticationLevelEnum
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WbemAuthenticationLevelEnum
 - wbemdisp/WbemAuthenticationLevelEnum
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wbemdisp.h
api_name:
 - WbemAuthenticationLevelEnum
---

# WbemAuthenticationLevelEnum enumeration


## -description

The 
<b>WbemAuthenticationLevelEnum</b> constants define the security authentication levels. These constants are used with 
<a href="/windows/desktop/WmiSdk/swbemsecurity">SWbemSecurity</a> and in moniker connections to WMI.

The WMI scripting type library, wbemdisp.tlb, defines these constants. Visual Basic applications can access this library.

Script languages must use one of the following:
<ul>
<li>
The short name. For example, for <b>WbemAuthenticationLevelPktPrivacy</b> use "PktPrivacy".


```vb

strComputer = "RemoteComputer"
Set objWMIServices = GetObject("WINMGMTS:" _
    & "{authenticationLevel=pktPrivacy}!\\" _
    & strComputer & "\ROOT\CIMV2")
```


</li>
<li>
Windows Script Host (WSH) XML file format in the script. For example, this means that the script can use the  <b>WbemAuthenticationLevelPkt</b> constant directly.

The following WSH script sets the authentication level. To run the script, save the text in a file with a .wsf extension.


```vb
<?xml version="1.0" encoding="US-ASCII"?>
<job>
<reference object="WbemScripting.SWbemLocator"/>
<script language="VBScript">
    set service = GetObject("winmgmts:")
    ' Following line uses a symbolic 
    ' constant from the WMI type library
    service.Security_.authenticationLevel = _
        WbemAuthenticationLevelPktPrivacy
</script>
</job>

```

For more information, see 
<a href="/windows/desktop/WmiSdk/using-the-wmi-scripting-type-library">Using the WMI Scripting Type Library</a>.</li>
</ul>

## -enum-fields

### -field wbemAuthenticationLevelDefault:0

### -field wbemAuthenticationLevelNone:1

### -field wbemAuthenticationLevelConnect:2

### -field wbemAuthenticationLevelCall:3

### -field wbemAuthenticationLevelPkt:4

### -field wbemAuthenticationLevelPktIntegrity:5

### -field wbemAuthenticationLevelPktPrivacy:6

### -field WbemAuthenticationLevelCall

Short name: Call

Authenticates only at the beginning of each call when the server receives the request.

### -field WbemAuthenticationLevelConnect

Short name: Connect

Authenticates the credentials of the client only when the client establishes a relationship with the server.

### -field WbemAuthenticationLevelDefault

Short name: Default

WMI uses the default Windows Authentication setting.

### -field WbemAuthenticationLevelNone

Short name: None

Uses no authentication.

### -field WbemAuthenticationLevelPkt

Short name: Pkt

Authenticates that all data received is from the expected client.

### -field WbemAuthenticationLevelPktIntegrity

Short name: PktIntegrity

Authenticates and verifies that none of the data transferred between client and server has been modified.

### -field WbemAuthenticationLevelPktPrivacy

Short name: PktPrivacy

Authenticates all previous impersonation levels and encrypts the argument value of each remote procedure call.

## -see-also

<a href="/windows/desktop/WmiSdk/constructing-a-moniker-string">Constructing a Moniker String</a>



<a href="/windows/desktop/WmiSdk/swbemsecurity">SWbemSecurity</a>



<a href="/windows/desktop/WmiSdk/scripting-api-constants">Scripting API Constants</a>



<a href="/windows/desktop/WmiSdk/setting-security-on-an-asynchronous-call-in-vbscript">Setting Security on an Asynchronous Call in VBScript</a>



<a href="/windows/desktop/WmiSdk/setting-the-default-process-security-level-using-vbscript">Setting the Default Process Security Level Using VBScript</a>
