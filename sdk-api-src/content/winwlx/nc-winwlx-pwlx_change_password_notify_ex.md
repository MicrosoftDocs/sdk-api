---
UID: NC:winwlx.PWLX_CHANGE_PASSWORD_NOTIFY_EX
title: PWLX_CHANGE_PASSWORD_NOTIFY_EX
author: windows-sdk-content
description: Called by GINA to tell a specific network provider (or all network providers) that a password has changed.
old-location: security\wlxchangepasswordnotifyex.htm
tech.root: SecAuthN
ms.assetid: 2381bf3e-37d3-460a-acb2-e2d59cd7d847
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PWLX_CHANGE_PASSWORD_NOTIFY_EX, PWLX_CHANGE_PASSWORD_NOTIFY_EX callback, WlxChangePasswordNotifyEx, WlxChangePasswordNotifyEx callback function [Security], _gina_wlxchangepasswordnotifyex, security.wlxchangepasswordnotifyex, winwlx/WlxChangePasswordNotifyEx
ms.topic: callback
req.header: winwlx.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - winwlx.h
api_name:
 - WlxChangePasswordNotifyEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PWLX_CHANGE_PASSWORD_NOTIFY_EX callback function


## -description


<p class="CCE_Message">[The WlxChangePasswordNotifyEx function is no longer available for use as of Windows Server 2008 and Windows Vista.]

Called by <a href="https://msdn.microsoft.com/c9567a5b-bd56-4ae1-9eac-af0bb5a6842a">GINA</a> to tell a specific network provider (or all network providers) that a password has changed.
<div class="alert"><b>Note</b>   GINA DLLs are ignored in Windows Vista.</div><div> </div>In this way, GINA can pass a change password request through to a specific network provider.

This function supersedes the 
<a href="https://msdn.microsoft.com/53765f8f-50cb-40dd-888e-0e1ddbe76f7e">WlxChangePasswordNotify</a> function.


## -parameters




### -param hWlx [in]

Specifies the <a href="https://msdn.microsoft.com/031c898b-3b4d-4b29-811a-112da37b5e3d">Winlogon</a> handle passed to GINA in the 
<a href="https://msdn.microsoft.com/db03f2b3-0719-40be-8a42-04ab7110f711">WlxInitialize</a> call.


### -param pMprInfo [in]

Points to a 
<a href="https://msdn.microsoft.com/68098b26-c58d-45fb-aebe-780a73cded80">WLX_MPR_NOTIFY_INFO</a> structure that contains <a href="https://msdn.microsoft.com/4c4402e9-7455-4868-978f-3899a8fd86c1">Multiple Provider Router</a> (MPR) information. Winlogon will call 
<a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a> to free all the data pointed to by this structure when it is done with it.


### -param dwChangeInfo [in]

Changes the information flags from Network Provider API.


### -param ProviderName [in]

Specifies the name of a network provider, or <b>NULL</b> to allow the system to notify all network providers.


### -param Reserved [in]

Reserved. Must be set to zero.


## -returns



The <b>WlxChangePasswordNotifyEx</b> function returns zero if the function call succeeds. Any other value indicates an error.




## -remarks



This function supersedes the 
<a href="https://msdn.microsoft.com/53765f8f-50cb-40dd-888e-0e1ddbe76f7e">WlxChangePasswordNotify</a> function.




## -see-also




<a href="https://msdn.microsoft.com/68098b26-c58d-45fb-aebe-780a73cded80">WLX_MPR_NOTIFY_INFO</a>



<a href="https://msdn.microsoft.com/53765f8f-50cb-40dd-888e-0e1ddbe76f7e">WlxChangePasswordNotify</a>



<a href="https://msdn.microsoft.com/db03f2b3-0719-40be-8a42-04ab7110f711">WlxInitialize</a>
 

 

