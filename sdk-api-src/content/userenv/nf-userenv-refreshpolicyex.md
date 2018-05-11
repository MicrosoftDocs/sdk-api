---
UID: NF:userenv.RefreshPolicyEx
title: RefreshPolicyEx function
author: windows-driver-content
description: The RefreshPolicyEx function causes policy to be applied immediately on the computer. The extended function allows you to specify the type of policy refresh to apply.
old-location: policy\refreshpolicyex.htm
old-project: Policy
ms.assetid: 905ab96b-a7f2-4bb4-a539-385f78284644
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: RP_FORCE, RefreshPolicyEx, RefreshPolicyEx function [Group Policy], _win32_refreshpolicyex, policy.refreshpolicyex, userenv/RefreshPolicyEx
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: userenv.h
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
req.type-library: 
req.typenames: USB_UNICODE_NAME, *PUSB_UNICODE_NAME
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Userenv.dll
api_name:
-	RefreshPolicyEx
product: Windows
targetos: Windows
req.lib: Userenv.lib
req.dll: Userenv.dll
req.irql: 
req.product: Windows UI
---

# RefreshPolicyEx function


## -description


The
    <b>RefreshPolicyEx</b> function causes policy to be applied immediately on the computer. The extended function allows you to specify the type of policy refresh to apply.


## -parameters




### -param bMachine [in]

Specifies whether to refresh the computer policy or user policy. If this value is <b>TRUE</b>, the system refreshes the computer policy. If this value is <b>FALSE</b>, the system refreshes the user policy.


### -param dwOptions [in]

Specifies the type of policy refresh to apply. This parameter can be the following value.



#### RP_FORCE

Reapply all policies even if no policy change was detected.

Note that if there are any client-side extensions that can be applied at boot or logon time, (for example, an application installation extension), the extensions are re-applied at the next boot or logon, even if no policy change is detected.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



If you do not need to specify the <i>dwOptions</i> parameter, you can call the 
<a href="https://msdn.microsoft.com/e08cb006-d174-4506-87f0-580660bd4023">RefreshPolicy</a> function instead.

By default, policy is reapplied every 90 minutes.




## -see-also




<a href="https://msdn.microsoft.com/7c45666e-d7c7-4989-ad19-b1b230757a88">Group Policy
    Functions</a>



<a href="https://msdn.microsoft.com/1285ab5a-ea68-4c16-bc34-8ab2f3cfad35">Group Policy
    Overview</a>



<a href="https://msdn.microsoft.com/f639c11c-ee65-45b6-ba0d-f39c825b3d80">ProcessGroupPolicy</a>



<a href="https://msdn.microsoft.com/df77fece-6e81-4a85-847a-fef3ba775e93">ProcessGroupPolicyEx</a>



<a href="https://msdn.microsoft.com/e08cb006-d174-4506-87f0-580660bd4023">RefreshPolicy</a>
 

 

