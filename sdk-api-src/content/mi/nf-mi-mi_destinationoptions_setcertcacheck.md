---
UID: NF:mi.MI_DestinationOptions_SetCertCACheck
title: MI_DestinationOptions_SetCertCACheck function (mi.h)
author: windows-sdk-content
description: Enables or disables the CA certificate check for an SSL transport.
old-location: wmi_v2\mi_destinationoptions_setcertcacheck.htm
tech.root: wmi_v2
ms.assetid: 79ba5973-719a-4a6b-94d1-04aff7e526aa
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MI_DestinationOptions_SetCertCACheck, MI_DestinationOptions_SetCertCACheck function [Windows Management Infrastructure (MI)], mi/MI_DestinationOptions_SetCertCACheck, wmi_v2.mi_destinationoptions_setcertcacheck
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mi.h
api_name:
 - MI_DestinationOptions_SetCertCACheck
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
---

# MI_DestinationOptions_SetCertCACheck function


## -description


Enables or disables the CA certificate check for an SSL transport.


## -parameters




### -param options [in, out]

A pointer to a <a href="https://msdn.microsoft.com/7f835ff4-3917-497c-bfe9-ca335cc35938">MI_DestinationOptions</a> object returned from the <a href="https://msdn.microsoft.com/efaa1244-7fe4-4484-b9ac-e7309e2012b6">MI_Application_NewDestinationOptions</a> function.


### -param check

Boolean value where <b>MI_TRUE</b> means to enable the certificate CA check and <b>MI_FALSE</b> means to disable it.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.




## -remarks



If an SSL transport is not used, this setting is ignored.  By default, the certificate CA check is carried out.  This may need to be disabled if a self signed certificate is used on the server.



