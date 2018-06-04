---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# SendSAS function


## -description


Simulates a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">secure attention sequence</a> (SAS).


## -parameters




### -param AsUser [in]

<b>TRUE</b> if the caller is running as the current user; otherwise, <b>FALSE</b>.


## -returns



This function does not return a value.




## -remarks



To successfully call the <b>SendSAS</b> function, an application must either be running as a service or have the <b>uiAccess</b> attribute of the <b>requestedExecutionLevel</b> element set to "true" in its application manifest. If an application is not running as a service, it must be running as either the current user or the LocalSystem account to call <b>SendSAS</b>. In addition, if an application is not running as a service, <a href="https://msdn.microsoft.com/8a7ba726-c2a6-4b7b-b664-3c6fcfbfb221">User Account Control</a> must be turned on to call <b>SendSAS</b>. 

<div class="alert"><b>Important</b>  Applications with the <b>uiAccess</b> attribute set to "true" must be signed by using <a href="_inet_authenticode_node_entry">Authenticode</a>. In addition, the application must reside in a protected location in the file system. Currently, there are two allowable protected locations:<dl>
<dd><b>\Program Files\</b></dd>
<dd><b>\windows\system32\</b></dd>
</dl>
</div>
<div> </div>
The local security policy of a computer must be configured to allow services and applications to simulate a SAS. To configure the policy, modify settings in the Group Policy Editor (GPE) Microsoft Management Console (MMC) snap-in. The GPE settings that control delegation are in the following location:

<b>Computer Configuration | Administrative Templates | Windows Components | Windows Logon Options | Disable or enable software Secure Attention Sequence</b>

A service can impersonate the token of another process that calls that service. In this case, a call to the <b>SendSAS</b> function by that service simulates a SAS on the session associated with the impersonated token.

<b>Windows Server 2008 and Windows Vista:  </b>Sas.dll is not available natively. You must download the Windows 7 version of the Microsoft Windows Software Development Kit (SDK)  to use this function. In addition, an application must refer to Sas.dll to call this function.



