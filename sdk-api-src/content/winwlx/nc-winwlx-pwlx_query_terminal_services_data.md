---
UID: NC:winwlx.PWLX_QUERY_TERMINAL_SERVICES_DATA
title: PWLX_QUERY_TERMINAL_SERVICES_DATA
author: windows-sdk-content
description: Called by GINA to retrieve Terminal Services user configuration information after a user has logged on.
old-location: security\wlxqueryterminalservicesdata.htm
tech.root: secauthn
ms.assetid: a7b81d76-74de-44a8-92ad-765ad1f7013e
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: PWLX_QUERY_TERMINAL_SERVICES_DATA, PWLX_QUERY_TERMINAL_SERVICES_DATA callback, WlxQueryTerminalServicesData, WlxQueryTerminalServicesData callback function [Security], _gina_wlxqueryterminalservicesdata, security.wlxqueryterminalservicesdata, winwlx/WlxQueryTerminalServicesData
ms.prod: windows
ms.technology: windows-sdk
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
 - WlxQueryTerminalServicesData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PWLX_QUERY_TERMINAL_SERVICES_DATA callback function


## -description


<p class="CCE_Message">[The WlxQueryTerminalServicesData function is no longer available for use as of Windows Server 2008 and Windows Vista.]

Called by <a href="https://msdn.microsoft.com/c9567a5b-bd56-4ae1-9eac-af0bb5a6842a">GINA</a> to retrieve Terminal Services user configuration information after a user has logged on.
<div class="alert"><b>Note</b>   GINA DLLs are ignored in Windows Vista.</div><div> </div>

## -parameters




### -param hWlx [in]

Specifies the Winlogon handle passed to GINA in the 
<a href="https://msdn.microsoft.com/db03f2b3-0719-40be-8a42-04ab7110f711">WlxInitialize</a> call.


### -param pTSData [out]

Points to a structure that will contain the user configuration information specific to Terminal Services.


### -param *UserName [in]

Pointer to a null-terminated wide character string that specifies the name of the newly logged-on user.


### -param *Domain [in]

Pointer to a null-terminated wide character string that specifies the newly logged-on user's domain.


## -returns



The <b>WlxQueryTerminalServicesData</b> function returns zero if the user-configuration information was retrieved successfully. Otherwise, it returns an error code.




## -remarks



<b>WlxQueryTerminalServicesData</b> should be called from within GINA's implementation of 
<a href="https://msdn.microsoft.com/7f3996b6-7c99-42c5-a39f-8c67ff19a580">WlxLoggedOutSAS</a> after a user has been authenticated.

In order to access this function, the GINA DLL must use the 
<a href="https://msdn.microsoft.com/47e343b8-ee54-45de-98c6-0ec75b45aa90">WLX_DISPATCH_VERSION_1_3</a> structure, and set the Winlogon version to at least WLX_VERSION_1_3 in its 
<a href="https://msdn.microsoft.com/9e7bab30-5cc6-4c55-82e4-d888e1af59ed">WlxNegotiate</a> call.




## -see-also




<a href="https://msdn.microsoft.com/47e343b8-ee54-45de-98c6-0ec75b45aa90">WLX_DISPATCH_VERSION_1_3</a>



<a href="https://msdn.microsoft.com/4f9f56dd-13cf-4125-90d0-4858a6c141be">WlxDisconnect</a>



<a href="https://msdn.microsoft.com/7f3996b6-7c99-42c5-a39f-8c67ff19a580">WlxLoggedOutSAS</a>



<a href="https://msdn.microsoft.com/9e7bab30-5cc6-4c55-82e4-d888e1af59ed">WlxNegotiate</a>



<a href="https://msdn.microsoft.com/b563606d-f4d5-48d7-914d-a11ed5f536a1">WlxQueryClientCredentials</a>



<a href="https://msdn.microsoft.com/bb36254c-0696-4f3f-89d7-332837ec3a75">WlxWin31Migrate</a>
 

 

