---
UID: NE:wbemdisp.WbemImpersonationLevelEnum
title: WbemImpersonationLevelEnum (wbemdisp.h)
description: Define the security impersonation levels. These constants are used with SWbemSecurity.
helpviewer_keywords: ["WbemImpersonationLevelEnum","WbemImpersonationLevelEnum enumeration [Windows Management Instrumentation]","_hmm_wbemimpersonationlevelenum","wbemImpersonationLevelAnonymous","wbemImpersonationLevelDelegate","wbemImpersonationLevelIdentify","wbemImpersonationLevelImpersonate","wbemdisp/WbemImpersonationLevelEnum","wbemdisp/wbemImpersonationLevelAnonymous","wbemdisp/wbemImpersonationLevelDelegate","wbemdisp/wbemImpersonationLevelIdentify","wbemdisp/wbemImpersonationLevelImpersonate","wmi.wbemimpersonationlevelenum"]
old-location: wmi\wbemimpersonationlevelenum.htm
tech.root: wmi
ms.assetid: 4a6d92a6-82d1-4426-8175-89cf9495c448
ms.date: 12/05/2018
ms.keywords: WbemImpersonationLevelEnum, WbemImpersonationLevelEnum enumeration [Windows Management Instrumentation], _hmm_wbemimpersonationlevelenum, wbemImpersonationLevelAnonymous, wbemImpersonationLevelDelegate, wbemImpersonationLevelIdentify, wbemImpersonationLevelImpersonate, wbemdisp/WbemImpersonationLevelEnum, wbemdisp/wbemImpersonationLevelAnonymous, wbemdisp/wbemImpersonationLevelDelegate, wbemdisp/wbemImpersonationLevelIdentify, wbemdisp/wbemImpersonationLevelImpersonate, wmi.wbemimpersonationlevelenum
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
req.typenames: WbemImpersonationLevelEnum
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WbemImpersonationLevelEnum
 - wbemdisp/WbemImpersonationLevelEnum
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
 - WbemImpersonationLevelEnum
---

# WbemImpersonationLevelEnum enumeration


## -description

The 
WbemImpersonationLevelEnum constants define the security impersonation levels. These constants are used with 
<a href="/windows/desktop/WmiSdk/swbemsecurity">SWbemSecurity</a>.

The WMI scripting type library, wbemdisp.tlb, defines these constants. Visual Basic applications can access this library.

Script languages must use one of the following:
<ul>
<li>
The short name. For example, for <b>wbemImpersonationLevelImpersonate</b> use "Impersonate".

The following VBScript code example uses the short name.


```vb
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=Impersonate}!\\" _
    & strComputer & "\root\cimv2")
```


</li>
<li>
Windows Script Host (WSH) XML file format in the script. For example, this means that the script can use the  <b>wbemImpersonationLevelImpersonate</b> constant directly.

The following WSH script sets the impersonation level. To run the script, save the text in a file with a .wsf extension.


```vb
<?xml version="1.0" encoding="US-ASCII"?>
<job>
<reference object="WbemScripting.SWbemLocator"/>
<script language="VBScript">
    set service = GetObject("winmgmts:")
    ' Following line uses a symbolic 
    ' constant from the WMI type library
    service.Security_.impersonationLevel = _
        wbemImpersonationLevelDelegate
</script>
</job>
```


For more information, see 
<a href="/windows/desktop/WmiSdk/using-the-wmi-scripting-type-library">Using the WMI Scripting Type Library</a>.

</li>
</ul>

## -enum-fields

### -field wbemImpersonationLevelAnonymous:1

Short name: Anonymous

Hides the credentials of the caller. Calls to WMI may fail with this impersonation level.

### -field wbemImpersonationLevelIdentify:2

Short name: Identify

Allows objects to query the credentials of the caller. Calls to WMI may fail with this impersonation level.

### -field wbemImpersonationLevelImpersonate:3

Short name: Impersonate

Allows objects to use the credentials of the caller. This is the recommended impersonation level for Scripting API for WMI calls.

### -field wbemImpersonationLevelDelegate:4

Short name: Delegate

Allows objects to permit other objects to use the credentials of the caller. This impersonation will work with Scripting API for WMI calls but may constitute an unnecessary security risk.

## -see-also

<a href="/windows/desktop/WmiSdk/swbemsecurity">SWbemSecurity</a>



<a href="/windows/desktop/WmiSdk/scripting-api-constants">Scripting API
    Constants</a>



<a href="/windows/desktop/WmiSdk/setting-client-application-process-security">Setting Client_Application_Process Security</a>
