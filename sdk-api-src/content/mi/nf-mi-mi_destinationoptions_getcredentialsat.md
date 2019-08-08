---
UID: NF:mi.MI_DestinationOptions_GetCredentialsAt
title: MI_DestinationOptions_GetCredentialsAt function (mi.h)
author: windows-sdk-content
description: Get the credentials at the specified index.
old-location: wmi_v2\mi_destinationoptions_getcredentialsat.htm
tech.root: wmi_v2
ms.assetid: 605f6486-f7d4-433e-9f56-49a868de9e8e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MI_DestinationOptions_GetCredentialsAt, MI_DestinationOptions_GetCredentialsAt function [Windows Management Infrastructure (MI)], mi/MI_DestinationOptions_GetCredentialsAt, wmi_v2.mi_destinationoptions_getcredentialsat
ms.topic: function
f1_keywords:
- mi/MI_DestinationOptions_GetCredentialsAt
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
- MI_DestinationOptions_GetCredentialsAt
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
---

# MI_DestinationOptions_GetCredentialsAt function


## -description


Get the credentials at the specified index.


## -parameters




### -param options [in]


<a href="https://docs.microsoft.com/windows/desktop/api/mi/ns-mi-mi_destinationoptions">MI_DestinationOptions</a> object returned from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_newdestinationoptions">MI_Application_NewDestinationOptions</a>.


### -param index

Zero-based index of the credentials.


### -param optionName

Returned name of the credentials option.


### -param credentials [out]

Returned <a href="https://docs.microsoft.com/windows/desktop/api/mi/ns-mi-mi_usercredentials">MI_UserCredentials</a> structure. If the credentials include a password, it will be filled with 6 asterisks for security purposes.


### -param flags [out, optional]

Returned credentials option flags.


## -returns



A value of the <a href="https://docs.microsoft.com/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.



