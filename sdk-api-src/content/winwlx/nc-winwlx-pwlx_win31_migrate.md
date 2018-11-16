---
UID: NC:winwlx.PWLX_WIN31_MIGRATE
title: PWLX_WIN31_MIGRATE
author: windows-sdk-content
description: Called by a replacement GINA DLL if Terminal Services is enabled. GINA calls this function to complete the setup of the Terminal Services client.
old-location: security\wlxwin31migrate.htm
tech.root: SecAuthN
ms.assetid: bb36254c-0696-4f3f-89d7-332837ec3a75
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: PWLX_WIN31_MIGRATE, PWLX_WIN31_MIGRATE callback, WlxWin31Migrate, WlxWin31Migrate callback function [Security], _gina_wlxwin31migrate, security.wlxwin31migrate, winwlx/WlxWin31Migrate
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - WlxWin31Migrate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PWLX_WIN31_MIGRATE callback function


## -description


<p class="CCE_Message">[The WlxWin31Migrate function is no longer available for use as of Windows Server 2008 and Windows Vista.]

Called by a replacement GINA DLL if Terminal Services is enabled.
			
				<a href="https://msdn.microsoft.com/c9567a5b-bd56-4ae1-9eac-af0bb5a6842a">GINA</a> calls this function to complete the setup of the Terminal Services client.
<div class="alert"><b>Note</b>   GINA DLLs are ignored in Windows Vista.</div><div> </div>

## -parameters




### -param hWlx [in]

Specify the handle received in the call to 
<a href="https://msdn.microsoft.com/db03f2b3-0719-40be-8a42-04ab7110f711">WlxInitialize</a>.


## -returns



This function has no return values.




## -remarks



GINA needs to call this function before starting the shell, so that the migration and setup will be complete before the shell starts, but after it has processed any logon scripts.

In order to use this function, the GINA DLL must specify the 
<a href="https://msdn.microsoft.com/47e343b8-ee54-45de-98c6-0ec75b45aa90">WLX_DISPATCH_VERSION_1_3</a> structure in its call to 
<a href="https://msdn.microsoft.com/db03f2b3-0719-40be-8a42-04ab7110f711">WlxInitialize</a>, and set the Winlogon version to at least WLX_VERSION_1_3 in its 
<a href="https://msdn.microsoft.com/9e7bab30-5cc6-4c55-82e4-d888e1af59ed">WlxNegotiate</a> call.

Other Winlogon support functions that may be called when Terminal Services is enabled are <a href="https://msdn.microsoft.com/4f9f56dd-13cf-4125-90d0-4858a6c141be">WlxDisconnect</a>, <a href="https://msdn.microsoft.com/b563606d-f4d5-48d7-914d-a11ed5f536a1">WlxQueryClientCredentials</a>, and <a href="https://msdn.microsoft.com/dfa12961-1552-4531-8f79-d44fb2a46e74">WlxQueryInetConnectorCredentials</a>.




## -see-also




<a href="https://msdn.microsoft.com/47e343b8-ee54-45de-98c6-0ec75b45aa90">WLX_DISPATCH_VERSION_1_3</a>



<a href="https://msdn.microsoft.com/4f9f56dd-13cf-4125-90d0-4858a6c141be">WlxDisconnect</a>



<a href="https://msdn.microsoft.com/9e7bab30-5cc6-4c55-82e4-d888e1af59ed">WlxNegotiate</a>



<a href="https://msdn.microsoft.com/b563606d-f4d5-48d7-914d-a11ed5f536a1">WlxQueryClientCredentials</a>



<a href="https://msdn.microsoft.com/dfa12961-1552-4531-8f79-d44fb2a46e74">WlxQueryInetConnectorCredentials</a>
 

 

