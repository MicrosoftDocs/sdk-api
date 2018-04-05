---
UID: NF:mi.MI_DestinationOptions_SetCertRevocationCheck
title: MI_DestinationOptions_SetCertRevocationCheck function
author: windows-driver-content
description: Enables or disables the certificate revocation when communicating over SSL.
old-location: wmi_v2\mi_destinationoptions_setcertrevocationcheck.htm
old-project: wmi_v2
ms.assetid: 941d1649-a4b1-4160-9917-a94afe0b8cd6
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: MI_DestinationOptions_SetCertRevocationCheck, MI_DestinationOptions_SetCertRevocationCheck function [Windows Management Infrastructure (MI)], mi/MI_DestinationOptions_SetCertRevocationCheck, wmi_v2.mi_destinationoptions_setcertrevocationcheck
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MI_Type
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Mi.h
api_name:
-	MI_DestinationOptions_SetCertRevocationCheck
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_DestinationOptions_SetCertRevocationCheck function


## -description


Enables or disables the certificate revocation when communicating over SSL.


## -parameters




### -param options [in, out]

A pointer to a <a href="https://msdn.microsoft.com/7f835ff4-3917-497c-bfe9-ca335cc35938">MI_DestinationOptions</a> object returned from <a href="https://msdn.microsoft.com/efaa1244-7fe4-4484-b9ac-e7309e2012b6">MI_Application_NewDestinationOptions</a>.


### -param check

A Boolean value, where <b>MI_TRUE</b> means the server's certificate will be checked for revocation, while <b>MI_FALSE</b> means the certificate will not be checked.


## -see-also




<a href="https://msdn.microsoft.com/efaa1244-7fe4-4484-b9ac-e7309e2012b6">MI_Application_NewDestinationOptions</a>



<a href="https://msdn.microsoft.com/7f835ff4-3917-497c-bfe9-ca335cc35938">MI_DestinationOptions</a>



<a href="https://msdn.microsoft.com/85af8514-a448-44c4-b1ad-f0a6b5c4a8a4">MI_DestinationOptions_GetCertRevocationCheck</a>
 

 

