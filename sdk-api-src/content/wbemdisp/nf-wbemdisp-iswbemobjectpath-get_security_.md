---
UID: NF:wbemdisp.ISWbemObjectPath.get_Security_
title: ISWbemObjectPath::get_Security_
author: windows-sdk-content
description: The Security property of the SWbemObjectPath object is used to get or set the security components of an object path.
old-location: wmi\swbemobjectpath_security_.htm
old-project: WmiSdk
ms.assetid: 26e5e990-3b78-41b6-83c4-ba0d8b0d2f00
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: ISWbemObjectPath interface [Windows Management Instrumentation],Security_ property, ISWbemObjectPath.get_Security_, ISWbemObjectPath::get_Security_, SWbemObjectPath object [Windows Management Instrumentation],Security_ property, SWbemObjectPath.Security_, Security_ property [Windows Management Instrumentation], Security_ property [Windows Management Instrumentation],ISWbemObjectPath interface, Security_ property [Windows Management Instrumentation],SWbemObjectPath object, _hmm_swbemobjectpath.security_, get_Security_, wmi.swbemobjectpath_security_
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
 - SWbemObjectPath.Security_
 - ISWbemObjectPath.Security_
 - ISWbemObjectPath.get_Security_
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemObjectPath::get_Security_


## -description


The <b>Security</b> property of the 
<a href="https://msdn.microsoft.com/f2cf489d-d2a9-4926-84cf-fb33fe3d726a">SWbemObjectPath</a> object is used to get or set the security components of an object path. Note that it is not used to set security attributes of the 
<b>SWbemObjectPath</b> object itself. It is used only to represent the security components of the path for an 
<a href="https://msdn.microsoft.com/51ea2c01-04e8-4b1c-bc82-ac96ba8b6eee">SWbemLocator</a> object. This property is an 
<a href="https://msdn.microsoft.com/794587fa-5feb-455b-be28-ecfaa25625ad">SWbemSecurity</a> object.
<div class="alert"><b>Note</b>  Setting the <a href="https://msdn.microsoft.com/add77267-d62f-4ee4-a0ff-8ca06a6bf7cd">Security_</a> property of an <a href="https://msdn.microsoft.com/00f5317e-eb8e-42f9-bada-963e11aadda4">SWbemObjectPath</a>  object to <b>NULL</b> grants unlimited access to everyone at all times. For more information, see <a href="https://msdn.microsoft.com/794587fa-5feb-455b-be28-ecfaa25625ad">SWbemSecurity</a>.</div><div> </div>For more information, see 
<a href="https://msdn.microsoft.com/889e6322-96f6-4a24-a084-e3b7bfa94a40">Document Conventions for the Scripting API</a>.

This property is read-only.


## -parameters


## -see-also




<a href="https://msdn.microsoft.com/c0d18827-6b36-4817-8cd9-06cd0f267b28">Creating a WMI Application or Script</a>



<a href="https://msdn.microsoft.com/f2cf489d-d2a9-4926-84cf-fb33fe3d726a">SWbemObjectPath</a>



<a href="https://msdn.microsoft.com/790b4e40-9b92-464a-a774-dec0b75cedee">Setting Client_Application_Process Security</a>
 

 

