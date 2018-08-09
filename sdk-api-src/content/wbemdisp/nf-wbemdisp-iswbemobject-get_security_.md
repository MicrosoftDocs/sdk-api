---
UID: NF:wbemdisp.ISWbemObject.get_Security_
title: ISWbemObject::get_Security_
author: windows-sdk-content
description: The Security_ property of the SWbemObject object is used to read, or set the security settings for an SWbemObject object.
old-location: wmi\swbemobject_security_.htm
old-project: WmiSdk
ms.assetid: add77267-d62f-4ee4-a0ff-8ca06a6bf7cd
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: ISWbemObject interface [Windows Management Instrumentation],Security_ property, ISWbemObject.get_Security_, ISWbemObject::get_Security_, SWbemObject object [Windows Management Instrumentation],Security_ property, SWbemObject.Security_, Security_ property [Windows Management Instrumentation], Security_ property [Windows Management Instrumentation],ISWbemObject interface, Security_ property [Windows Management Instrumentation],SWbemObject object, _hmm_swbemobject.security_, get_Security_, wmi.swbemobject_security_
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
 - SWbemObject.Security_
 - ISWbemObject.Security_
 - ISWbemObject.get_Security_
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemObject::get_Security_


## -description


The 
<b>Security_</b> property of the 
<a href="https://msdn.microsoft.com/d303ec1a-5e0c-4a5e-8ed3-ed353a138755">SWbemObject</a> object is used to read, or set the security settings for an 
<b>SWbemObject</b> object. This property is an 
<a href="https://msdn.microsoft.com/794587fa-5feb-455b-be28-ecfaa25625ad">SWbemSecurity</a> object.  The security settings in this object  do not indicate the   authentication, impersonation, or privilege settings made on a connection to Windows Management Instrumentation (WMI), or the security in effect for the proxy when an object is delivered to a sink in an asynchronous call. For more information, see <a href="https://msdn.microsoft.com/88a2538a-ae30-4a1a-9d16-f0cd9419b2ed">Maintaining WMI Security</a>.
<div class="alert"><b>Note</b>  Setting the <b>Security_</b> property of an <a href="https://msdn.microsoft.com/d303ec1a-5e0c-4a5e-8ed3-ed353a138755">SWbemObject</a>  object to <b>NULL</b> grants unlimited access to everyone all the time. For more information, see <a href="https://msdn.microsoft.com/794587fa-5feb-455b-be28-ecfaa25625ad">SWbemSecurity</a>.</div><div> </div>For an explanation of this syntax, see 
<a href="https://msdn.microsoft.com/889e6322-96f6-4a24-a084-e3b7bfa94a40">Document Conventions for the Scripting API</a>.

This property is read-only.


## -parameters


## -see-also




<a href="https://msdn.microsoft.com/c0d18827-6b36-4817-8cd9-06cd0f267b28">Creating a WMI Application or Script</a>



<a href="https://msdn.microsoft.com/f9400597-81bb-44a8-80dc-aba0160aea26">Privilege Constants</a>



<a href="https://msdn.microsoft.com/d303ec1a-5e0c-4a5e-8ed3-ed353a138755">SWbemObject</a>



<a href="https://msdn.microsoft.com/794587fa-5feb-455b-be28-ecfaa25625ad">SWbemSecurity</a>



<a href="https://msdn.microsoft.com/790b4e40-9b92-464a-a774-dec0b75cedee">Setting Client_Application_Process Security</a>



<a href="https://msdn.microsoft.com/1789b25a-e9a0-42a3-97c2-077e902a2f41">WbemAuthenticationLevelEnum</a>



<a href="https://msdn.microsoft.com/4a6d92a6-82d1-4426-8175-89cf9495c448">WbemImpersonationLevelEnum</a>



<a href="https://msdn.microsoft.com/235a1115-d8c4-4334-a4e0-fc539da4d2ae">WbemPrivilegeEnum</a>
 

 

