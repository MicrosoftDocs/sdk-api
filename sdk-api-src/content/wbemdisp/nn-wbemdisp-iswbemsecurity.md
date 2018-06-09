---
UID: NN:wbemdisp.ISWbemSecurity
title: ISWbemSecurity
author: windows-sdk-content
description: The SWbemSecurity object gets or sets security settings, such as privileges, COM impersonations, and authentication levels assigned to an object.
old-location: wmi\swbemsecurity.htm
old-project: WmiSdk
ms.assetid: 794587fa-5feb-455b-be28-ecfaa25625ad
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: ISWbemSecurity, SWbemSecurity, SWbemSecurity object [Windows Management Instrumentation], SWbemSecurity object [Windows Management Instrumentation],described, _hmm_swbemsecurity, wbemdisp/SWbemSecurity, wmi.swbemsecurity
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wbemdisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: Wbemdisp.tlb
tech.root: 
req.typenames: WbemTimeout
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wbemdisp.dll
api_name:
 - SWbemSecurity
 - ISWbemSecurity
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemSecurity interface


## -description


The 
<b>SWbemSecurity</b> object gets or sets  security settings,  such as privileges, COM impersonations, and authentication levels assigned to an object. The 
<a href="https://msdn.microsoft.com/51ea2c01-04e8-4b1c-bc82-ac96ba8b6eee">SWbemLocator</a>, 
<a href="https://msdn.microsoft.com/7fcfa404-2fe6-42e5-85ac-64536f6d2a44">SWbemServices</a>, 
<a href="https://msdn.microsoft.com/d303ec1a-5e0c-4a5e-8ed3-ed353a138755">SWbemObject</a>, 
<a href="https://msdn.microsoft.com/00f5317e-eb8e-42f9-bada-963e11aadda4">SWbemObjectSet</a>, 
<a href="https://msdn.microsoft.com/f2cf489d-d2a9-4926-84cf-fb33fe3d726a">SWbemObjectPath</a>, 
<a href="https://msdn.microsoft.com/11a652fa-29e8-437b-8e62-e28e56a8a38d">SWbemLastError</a>, and 
<a href="https://msdn.microsoft.com/7efd5e6a-4311-4d20-8b05-e9208eec098a">SWbemEventSource</a> objects have a <b>Security_</b>  property, which is the  
<b>SWbemSecurity</b> object. When you retrieve an instance or view the  WMI security log, you might need to set the properties of the 
<b>Security_</b> object.

The VBScript   <a href="https://msdn.microsoft.com/en-us/library/xzysf6hc(v=vs.84).aspx">CreateObject</a> call  cannot create the Security object.  The security settings in this object  do not identify the    authentication, impersonation, or privilege settings  on a  connection to WMI, or  the security in effect for the proxy when an object is delivered to a sink in an asynchronous call. For more information, see <a href="https://msdn.microsoft.com/88a2538a-ae30-4a1a-9d16-f0cd9419b2ed">Maintaining WMI Security</a>.


## -see-also




<a href="https://msdn.microsoft.com/88a2538a-ae30-4a1a-9d16-f0cd9419b2ed">Maintaining WMI Security</a>



<a href="https://msdn.microsoft.com/91bc0fad-1a4b-4b48-b5a0-1a6502d2ab26">Scripting API Objects</a>



<a href="https://msdn.microsoft.com/790b4e40-9b92-464a-a774-dec0b75cedee">Setting Client_Application_Process Security</a>



<a href="https://msdn.microsoft.com/1789b25a-e9a0-42a3-97c2-077e902a2f41">WbemAuthenticationLevelEnum</a>



<a href="https://msdn.microsoft.com/4a6d92a6-82d1-4426-8175-89cf9495c448">WbemImpersonationLevelEnum</a>



<a href="https://msdn.microsoft.com/235a1115-d8c4-4334-a4e0-fc539da4d2ae">WbemPrivilegeEnum</a>
 

 

