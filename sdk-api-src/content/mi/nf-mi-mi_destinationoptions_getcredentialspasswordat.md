---
UID: NF:mi.MI_DestinationOptions_GetCredentialsPasswordAt
title: MI_DestinationOptions_GetCredentialsPasswordAt function (mi.h)
description: Gets a credentials password based on a specified index.
helpviewer_keywords: ["MI_DestinationOptions_GetCredentialsPasswordAt","MI_DestinationOptions_GetCredentialsPasswordAt function [Windows Management Infrastructure (MI)]","mi/MI_DestinationOptions_GetCredentialsPasswordAt","wmi_v2.mi_destinationoptions_getcredentialspasswordat"]
old-location: wmi_v2\mi_destinationoptions_getcredentialspasswordat.htm
tech.root: wmi_v2
ms.assetid: 95ea5856-5b15-4522-9652-a7b52d89055a
ms.date: 12/05/2018
ms.keywords: MI_DestinationOptions_GetCredentialsPasswordAt, MI_DestinationOptions_GetCredentialsPasswordAt function [Windows Management Infrastructure (MI)], mi/MI_DestinationOptions_GetCredentialsPasswordAt, wmi_v2.mi_destinationoptions_getcredentialspasswordat
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
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
f1_keywords:
 - MI_DestinationOptions_GetCredentialsPasswordAt
 - mi/MI_DestinationOptions_GetCredentialsPasswordAt
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mi.h
api_name:
 - MI_DestinationOptions_GetCredentialsPasswordAt
---

# MI_DestinationOptions_GetCredentialsPasswordAt function


## -description

Gets a credentials password based on  a specified index.

## -parameters

### -param options [in]

<a href="/windows/desktop/api/mi/ns-mi-mi_destinationoptions">MI_DestinationOptions</a> object returned from <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_newdestinationoptions">MI_Application_NewDestinationOptions</a>.

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

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.

## -remarks

Passwords should not be stored in memory for long periods of time in an unencrypted manner, as there are ways to snoop for them. After using the password, call the <a href="/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)">SecureZeroMemory</a> function to clear out the password before deleting it.