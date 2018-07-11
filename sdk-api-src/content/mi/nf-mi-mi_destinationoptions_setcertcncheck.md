---
UID: NF:mi.MI_DestinationOptions_SetCertCNCheck
title: MI_DestinationOptions_SetCertCNCheck function
author: windows-sdk-content
description: Enables or disables the certificate CN check when an SSL transport is used.
old-location: wmi_v2\mi_destinationoptions_setcertcncheck.htm
old-project: wmi_v2
ms.assetid: 19b8bcf5-192a-4e14-9efe-3124b8051e04
ms.author: windowssdkdev
ms.date: 06/14/2018
ms.keywords: MI_DestinationOptions_SetCertCNCheck, MI_DestinationOptions_SetCertCNCheck function [Windows Management Infrastructure (MI)], mi/MI_DestinationOptions_SetCertCNCheck, wmi_v2.mi_destinationoptions_setcertcncheck
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MI_Type
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mi.h
api_name:
 - MI_DestinationOptions_SetCertCNCheck
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_DestinationOptions_SetCertCNCheck function


## -description


Enables or disables the certificate CN check when an SSL transport is used.


## -parameters




### -param options [in, out]

A pointer to a <a href="https://msdn.microsoft.com/7f835ff4-3917-497c-bfe9-ca335cc35938">MI_DestinationOptions</a> object returned from <a href="https://msdn.microsoft.com/efaa1244-7fe4-4484-b9ac-e7309e2012b6">MI_Application_NewDestinationOptions</a>.


### -param check

Boolean value where <b>MI_TRUE</b> means to enable the certificate CN check and <b>MI_FALSE</b> means to disable it.


## -remarks



The certificate CN is checked by default.




## -see-also




<a href="https://msdn.microsoft.com/efaa1244-7fe4-4484-b9ac-e7309e2012b6">MI_Application_NewDestinationOptions</a>



<a href="https://msdn.microsoft.com/7f835ff4-3917-497c-bfe9-ca335cc35938">MI_DestinationOptions</a>



<a href="https://msdn.microsoft.com/8f6a4f66-29cf-486b-9114-05cd357a32bf">MI_DestinationOptions_GetCertCNCheck</a>
 

 

