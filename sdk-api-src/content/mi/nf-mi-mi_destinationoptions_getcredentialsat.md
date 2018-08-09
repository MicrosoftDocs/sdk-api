---
UID: NF:mi.MI_DestinationOptions_GetCredentialsAt
title: MI_DestinationOptions_GetCredentialsAt function
author: windows-sdk-content
description: Get the credentials at the specified index.
old-location: wmi_v2\mi_destinationoptions_getcredentialsat.htm
old-project: wmi_v2
ms.assetid: 605f6486-f7d4-433e-9f56-49a868de9e8e
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: MI_DestinationOptions_GetCredentialsAt, MI_DestinationOptions_GetCredentialsAt function [Windows Management Infrastructure (MI)], mi/MI_DestinationOptions_GetCredentialsAt, wmi_v2.mi_destinationoptions_getcredentialsat
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
 - MI_DestinationOptions_GetCredentialsAt
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_DestinationOptions_GetCredentialsAt function


## -description


Get the credentials at the specified index.


## -parameters




### -param options [in]


<a href="https://msdn.microsoft.com/7f835ff4-3917-497c-bfe9-ca335cc35938">MI_DestinationOptions</a> object returned from <a href="https://msdn.microsoft.com/efaa1244-7fe4-4484-b9ac-e7309e2012b6">MI_Application_NewDestinationOptions</a>.


### -param index

Zero-based index of the credentials.


### -param optionName

Returned name of the credentials option.


### -param credentials [out]

Returned <a href="https://msdn.microsoft.com/30191cd1-00de-42ef-ac95-5e174d273c80">MI_UserCredentials</a> structure. If the credentials include a password, it will be filled with 6 asterisks for security purposes.


### -param flags [out, optional]

Returned credentials option flags.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.



