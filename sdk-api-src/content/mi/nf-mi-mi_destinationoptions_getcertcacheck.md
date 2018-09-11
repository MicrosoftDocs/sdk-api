---
UID: NF:mi.MI_DestinationOptions_GetCertCACheck
title: MI_DestinationOptions_GetCertCACheck function
author: windows-sdk-content
description: Gets the server certificate CA check value.
old-location: wmi_v2\mi_destinationoptions_getcertcacheck.htm
tech.root: wmi_v2
ms.assetid: 9b1b5bca-4e1f-4c37-9df4-9101f40f1b97
ms.author: windowssdkdev
ms.date: 08/13/2018
ms.keywords: MI_DestinationOptions_GetCertCACheck, MI_DestinationOptions_GetCertCACheck function [Windows Management Infrastructure (MI)], mi/MI_DestinationOptions_GetCertCACheck, wmi_v2.mi_destinationoptions_getcertcacheck
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
 - MI_DestinationOptions_GetCertCACheck
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
---

# MI_DestinationOptions_GetCertCACheck function


## -description


Gets the server certificate CA check value.


## -parameters




### -param options [in]


<a href="https://msdn.microsoft.com/7f835ff4-3917-497c-bfe9-ca335cc35938">MI_DestinationOptions</a> object returned from <a href="https://msdn.microsoft.com/efaa1244-7fe4-4484-b9ac-e7309e2012b6">MI_Application_NewDestinationOptions</a>.


### -param check [out]

Returned Boolean value indicating if the CA value will be checked (<b>MI_TRUE</b>) or not (<b>MI_FALSE</b>).


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.




## -remarks



All getters only return information that was previously added by the client. This is appropriate to all the getters of destination and operation options.



