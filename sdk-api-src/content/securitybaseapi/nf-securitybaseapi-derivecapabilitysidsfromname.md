---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# DeriveCapabilitySidsFromName function


## -description


    This function constructs two arrays of SIDs out of a capability name. 
    One is an array group SID with NT Authority, and the other is an array of 
    capability SIDs with AppAuthority.


## -parameters




### -param CapName [in]

Name of the capability in string form.


### -param CapabilityGroupSids [out]

The GroupSids with NTAuthority.


### -param CapabilityGroupSidCount [out]

The count of GroupSids in the array.


### -param CapabilitySids [out]

CapabilitySids with AppAuthority.


### -param CapabilitySidCount [out]

The count of CapabilitySid with AppAuthority.


## -returns



If the function succeeds, it returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



    The caller is expected to free the individual SIDs returned in each array by calling LocalFree.
    as well as memory allocated for the array itself.

    The SID computed for the application capability of legacy capabilities
    (published prior to Win10) will be the same as the published SIDs but the
    SID for the service group capability SID will be hash based.




