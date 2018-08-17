---
UID: NF:mi.MI_DestinationOptions_GetCredentialsPasswordAt
title: MI_DestinationOptions_GetCredentialsPasswordAt function
author: windows-sdk-content
description: Gets a credentials password based on a specified index.
old-location: wmi_v2\mi_destinationoptions_getcredentialspasswordat.htm
old-project: wmi_v2
ms.assetid: 95ea5856-5b15-4522-9652-a7b52d89055a
ms.author: windowssdkdev
ms.date: 08/13/2018
ms.keywords: MI_DestinationOptions_GetCredentialsPasswordAt, MI_DestinationOptions_GetCredentialsPasswordAt function [Windows Management Infrastructure (MI)], mi/MI_DestinationOptions_GetCredentialsPasswordAt, wmi_v2.mi_destinationoptions_getcredentialspasswordat
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: mi.h
req.include-header: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
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
 - MI_DestinationOptions_GetCredentialsPasswordAt
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_DestinationOptions_GetCredentialsPasswordAt function


## -description


Gets a credentials password based on  a specified index.


## -parameters




### -param options [in]


<a href="https://msdn.microsoft.com/7f835ff4-3917-497c-bfe9-ca335cc35938">MI_DestinationOptions</a> object returned from <a href="https://msdn.microsoft.com/efaa1244-7fe4-4484-b9ac-e7309e2012b6">MI_Application_NewDestinationOptions</a>.


### -param index

Zero-based index of the credentials password.


### -param optionName

A pointer to a null-terminated string containing the returned name of the option.


### -param password

Returned password. This memory should be freed for security purposes when finished.


### -param bufferLength [in]

Length of the <b>password</b> buffer. If 0, the <b>passwordLength</b> parameter will contain the buffer size needed to hold the password.


### -param passwordLength [out]

Returned amount of the <b>password</b> buffer used, including the null terminator.


### -param flags [out, optional]

Returned option flags.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.




## -remarks



Passwords should not be stored in memory for long periods of time in an unencrypted manner, as there are ways to snoop for them. After using the password, call the <a href="https://msdn.microsoft.com/2c4090a6-025b-4b7b-8f31-7e744ad51b39">SecureZeroMemory</a> function to clear out the password before deleting it.



