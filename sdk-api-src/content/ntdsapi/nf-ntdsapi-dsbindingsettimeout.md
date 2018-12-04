---
UID: NF:ntdsapi.DsBindingSetTimeout
title: DsBindingSetTimeout function
author: windows-sdk-content
description: The DsBindingSetTimeout function sets the timeout value that is honored by all RPC calls that use the specified binding handle. RPC calls that required more time than the timeout value are canceled.
old-location: ad\dsbindingsettimeout.htm
tech.root: ad
ms.assetid: abdaae89-fba3-4949-92a9-acd62898ec24
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: DsBindingSetTimeout, DsBindingSetTimeout function [Active Directory], ad.dsbindingsettimeout, ntdsapi/DsBindingSetTimeout
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ntdsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ntdsapi.lib
req.dll: Ntdsapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ntdsapi.dll
api_name:
 - DsBindingSetTimeout
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DsBindingSetTimeout function


## -description


The <b>DsBindingSetTimeout</b> function sets the timeout value
that is honored by all RPC calls that use the specified binding
handle. RPC calls that required more time than the timeout value are canceled.


## -parameters




### -param hDS [in]

Contains a directory service handle obtained from either the 
<a href="https://msdn.microsoft.com/c73cd16d-ccfd-4f61-b1c5-50130bef64d7">DSBind</a> or 
<a href="https://msdn.microsoft.com/708e3874-852c-4a57-bf4b-edaf98818fe5">DSBindWithCred</a> function.


### -param cTimeoutSecs [in]

Contains the new timeout value, in seconds.


## -returns



Returns <b>ERROR_SUCCESS</b> if successful or a Win32 or RPC error code otherwise. The following is a  possible error code.




## -see-also




<a href="https://msdn.microsoft.com/a92783c2-ffb8-473e-8484-1c05ca5453ff">Domain Controller and Replication Management Functions</a>



<a href="https://msdn.microsoft.com/c73cd16d-ccfd-4f61-b1c5-50130bef64d7">DsBind</a>



<a href="https://msdn.microsoft.com/708e3874-852c-4a57-bf4b-edaf98818fe5">DsBindWithCred</a>
 

 

