---
UID: NF:wbemdisp.ISWbemLocator.get_Security_
title: ISWbemLocator::get_Security_
author: windows-sdk-content
description: The Security_ property of the SWbemLocator object is used to read or set the security settings for an SWbemLocator object. This property is an SWbemSecurity object.
old-location: wmi\swbemlocator_security_.htm
old-project: WmiSdk
ms.assetid: 75987bef-21ae-4420-b069-afab90499218
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: ISWbemLocator interface [Windows Management Instrumentation],Security_ property, ISWbemLocator.get_Security_, ISWbemLocator::get_Security_, SWbemLocator object [Windows Management Instrumentation],Security_ property, SWbemLocator.Security_, Security_ property [Windows Management Instrumentation], Security_ property [Windows Management Instrumentation],ISWbemLocator interface, Security_ property [Windows Management Instrumentation],SWbemLocator object, _hmm_swbemlocator.security_, get_Security_, wmi.swbemlocator_security_
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
 - SWbemLocator.Security_
 - ISWbemLocator.Security_
 - ISWbemLocator.get_Security_
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemLocator::get_Security_


## -description


The 
<b>Security_</b> property of the 
<a href="https://msdn.microsoft.com/51ea2c01-04e8-4b1c-bc82-ac96ba8b6eee">SWbemLocator</a> object is used to read or set the security settings for an 
<b>SWbemLocator</b> object. This property is an 
<a href="https://msdn.microsoft.com/794587fa-5feb-455b-be28-ecfaa25625ad">SWbemSecurity</a> object.
<div class="alert"><b>Note</b>  Setting the <b>Security_</b> property of an <a href="https://msdn.microsoft.com/51ea2c01-04e8-4b1c-bc82-ac96ba8b6eee">SWbemLocator</a>  object to <b>NULL</b> grants unlimited access to everyone at all times. For more information, see <a href="https://msdn.microsoft.com/794587fa-5feb-455b-be28-ecfaa25625ad">SWbemSecurity</a>.</div><div> </div>For an explanation of this syntax, see 
<a href="https://msdn.microsoft.com/889e6322-96f6-4a24-a084-e3b7bfa94a40">Document Conventions for the Scripting API</a>.

This property is read-only.


## -parameters


## -remarks



The properties of an <b>SWbemLocator.Security_</b> object have no default values. If you attempt to get the value of 
<a href="https://msdn.microsoft.com/96c2e6a5-a91f-469d-bdd1-eaa20b176158">SWbemSecurity.AuthenticationLevel</a> or 
<a href="https://msdn.microsoft.com/cf57620b-7827-4552-a969-d25e5eb13a89">SWbemSecurity.ImpersonationLevel</a> on an 
<a href="https://msdn.microsoft.com/51ea2c01-04e8-4b1c-bc82-ac96ba8b6eee">SWbemLocator</a> object before you have set it, an <a href="https://msdn.microsoft.com/6accd7c9-cb12-4eba-aff0-0aa38324b4ff">wbemErrFailed</a> error results.




## -see-also




<a href="https://msdn.microsoft.com/c0d18827-6b36-4817-8cd9-06cd0f267b28">Creating a WMI Application or Script</a>



<a href="https://msdn.microsoft.com/65b923d5-5244-498d-9644-d4978fb84f85">Executing Privileged Operations Using VBScript</a>



<a href="https://msdn.microsoft.com/51ea2c01-04e8-4b1c-bc82-ac96ba8b6eee">SWbemLocator</a>



<a href="https://msdn.microsoft.com/794587fa-5feb-455b-be28-ecfaa25625ad">SWbemSecurity object</a>



<a href="https://msdn.microsoft.com/96ebaa9b-a062-4300-a637-8eb71cb80d1c">Securing a Remote WMI Connection</a>



<a href="https://msdn.microsoft.com/790b4e40-9b92-464a-a774-dec0b75cedee">Setting Client_Application_Process Security</a>
 

 

