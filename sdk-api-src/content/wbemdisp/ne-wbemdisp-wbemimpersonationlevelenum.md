---
UID: NE:wbemdisp.WbemImpersonationLevelEnum
title: WbemImpersonationLevelEnum
author: windows-sdk-content
description: Define the security impersonation levels. These constants are used with SWbemSecurity.
old-location: wmi\wbemimpersonationlevelenum.htm
old-project: WmiSdk
ms.assetid: 4a6d92a6-82d1-4426-8175-89cf9495c448
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: WbemImpersonationLevelEnum, WbemImpersonationLevelEnum enumeration [Windows Management Instrumentation], _hmm_wbemimpersonationlevelenum, wbemImpersonationLevelAnonymous, wbemImpersonationLevelDelegate, wbemImpersonationLevelIdentify, wbemImpersonationLevelImpersonate, wbemdisp/WbemImpersonationLevelEnum, wbemdisp/wbemImpersonationLevelAnonymous, wbemdisp/wbemImpersonationLevelDelegate, wbemdisp/wbemImpersonationLevelIdentify, wbemdisp/wbemImpersonationLevelImpersonate, wmi.wbemimpersonationlevelenum
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
req.typenames: WbemImpersonationLevelEnum
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wbemdisp.h
api_name:
 - WbemImpersonationLevelEnum
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# WbemImpersonationLevelEnum enumeration


## -description


The 
WbemImpersonationLevelEnum constants define the security impersonation levels. These constants are used with 
<a href="https://msdn.microsoft.com/794587fa-5feb-455b-be28-ecfaa25625ad">SWbemSecurity</a>.

The WMI scripting type library, wbemdisp.tlb, defines these constants. Visual Basic applications can access this library.

Script languages must use one of the following:
<ul>
<li>
The short name. For example, for <b>wbemImpersonationLevelImpersonate</b> use "Impersonate".

The following VBScript code example uses the short name.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Set objWMIService = GetObject("winmgmts:" _ 
    &amp; "{impersonationLevel=Impersonate}!\\" _
    &amp; strComputer &amp; "\root\cimv2")</pre>
</td>
</tr>
</table></span></div>
</li>
<li>
Windows Script Host (WSH) XML file format in the script. For example, this means that the script can use the  <b>wbemImpersonationLevelImpersonate</b> constant directly.

The following WSH script sets the impersonation level. To run the script, save the text in a file with a .wsf extension.

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
    service.Security_.impersonationLevel = _
        wbemImpersonationLevelDelegate
&lt;/script&gt;
&lt;/job&gt;</pre>
</td>
</tr>
</table></span></div>
For more information, see 
<a href="https://msdn.microsoft.com/6ef4e210-0733-4f2a-89c1-1a7aca5a19d9">Using the WMI Scripting Type Library</a>.

</li>
</ul>

## -enum-fields




### -field wbemImpersonationLevelAnonymous

Short name: Anonymous

Hides the credentials of the caller. Calls to WMI may fail with this impersonation level.


### -field wbemImpersonationLevelIdentify

Short name: Identify

Allows objects to query the credentials of the caller. Calls to WMI may fail with this impersonation level.


### -field wbemImpersonationLevelImpersonate

Short name: Impersonate

Allows objects to use the credentials of the caller. This is the recommended impersonation level for Scripting API for WMI calls.


### -field wbemImpersonationLevelDelegate

Short name: Delegate

Allows objects to permit other objects to use the credentials of the caller. This impersonation will work with Scripting API for WMI calls but may constitute an unnecessary security risk.


## -see-also




<a href="https://msdn.microsoft.com/794587fa-5feb-455b-be28-ecfaa25625ad">SWbemSecurity</a>



<a href="https://msdn.microsoft.com/feaab757-3167-420b-8f42-edced4cd4c53">Scripting API
    Constants</a>



<a href="https://msdn.microsoft.com/790b4e40-9b92-464a-a774-dec0b75cedee">Setting Client_Application_Process Security</a>
 

 

