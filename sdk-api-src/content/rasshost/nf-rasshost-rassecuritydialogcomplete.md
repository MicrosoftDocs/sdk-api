---
UID: NF:rasshost.RasSecurityDialogComplete
title: RasSecurityDialogComplete function
author: windows-driver-content
description: The RasSecurityDialogComplete function notifies the RAS server of the results of a third-party security authentication transaction.
old-location: rras\rassecuritydialogcomplete.htm
old-project: RRAS
ms.assetid: 9ebe8b85-7500-405f-98c2-6f51f3339629
ms.author: windowsdriverdev
ms.date: 5/21/2018
ms.keywords: RasSecurityDialogComplete, RasSecurityDialogComplete function [RAS], _ras_rassecuritydialogcomplete, rasshost/RasSecurityDialogComplete, rras.rassecuritydialogcomplete
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: rasshost.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: RAS_AUTH_ATTRIBUTE, *PRAS_AUTH_ATTRIBUTE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Rasman.dll
api_name:
-	RasSecurityDialogComplete
product: Windows
targetos: Windows
req.lib: 
req.dll: Rasman.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# RasSecurityDialogComplete function


## -description


The 
<b>RasSecurityDialogComplete</b> function notifies the RAS server of the results of a third-party security authentication transaction. A third-party RAS security DLL calls 
<b>RasSecurityDialogComplete</b> when it has completed its authentication of the remote user.

The RAS server passes a pointer to the 
<b>RasSecurityDialogComplete</b> function when the server calls the 
<a href="https://msdn.microsoft.com/19f4591b-ecae-478b-b110-c0d88c72f7eb">RasSecurityDialogBegin</a> entry point of the security DLL.
<div class="alert"><b>Note</b>  Windows Server 2008, 
  Windows Server 2003,
  Windows 2000 Server, and
  Windows NT Server 4.0 currently provide RAS security host support for serial devices only. Other types of connections, such as Integrated Services Digital Network (ISDN) or virtual private network (VPN) connections, are not supported.</div><div> </div>

## -parameters




### -param pSecMsg [in]

Pointer to the 
<a href="https://msdn.microsoft.com/7eab7bff-1c72-4382-980f-be4e58d60159">SECURITY_MESSAGE</a> structure that specifies the results of the authentication transaction.


## -returns



This function does not return a value.




## -remarks



When a security DLL has finished authenticating the remote user, it calls the 
<b>RasSecurityDialogComplete</b> function to report the results. The RAS server then performs a cleanup sequence. As part of this cleanup sequence, the RAS server calls the security DLL's 
<a href="https://msdn.microsoft.com/52274d37-baed-4ab9-8019-123ae7c5b0fc">RasSecurityDialogEnd</a> function to give the DLL an opportunity to perform its own cleanup, if necessary.




## -see-also




<a href="https://msdn.microsoft.com/44c000d7-2bb6-4fd8-ac5f-9d3850d857a0">RAS Server Administration Functions</a>



<a href="https://msdn.microsoft.com/19f4591b-ecae-478b-b110-c0d88c72f7eb">RasSecurityDialogBegin</a>



<a href="https://msdn.microsoft.com/52274d37-baed-4ab9-8019-123ae7c5b0fc">RasSecurityDialogEnd</a>



<a href="https://msdn.microsoft.com/5016fa0b-72eb-484e-b8d7-af9de2e25689">Remote Access Service (RAS) Overview</a>



<a href="https://msdn.microsoft.com/7eab7bff-1c72-4382-980f-be4e58d60159">SECURITY_MESSAGE</a>
 

 

