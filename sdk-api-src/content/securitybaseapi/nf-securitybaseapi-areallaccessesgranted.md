---
UID: NF:securitybaseapi.AreAllAccessesGranted
title: AreAllAccessesGranted function
author: windows-sdk-content
description: Checks whether a set of requested access rights has been granted. The access rights are represented as bit flags in an access mask.
old-location: security\areallaccessesgranted.htm
tech.root: secauthz
ms.assetid: 91349693-8667-49dd-a813-657497b7d467
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: AreAllAccessesGranted, AreAllAccessesGranted function [Security], _win32_areallaccessesgranted, security.areallaccessesgranted, securitybaseapi/AreAllAccessesGranted
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: securitybaseapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-1.dll
 - API-MS-Win-Security-base-l1-1-0.dll
 - API-MS-Win-Security-base-l1-2-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Security-Base-L1-2-1.dll
api_name:
 - AreAllAccessesGranted
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# AreAllAccessesGranted function


## -description


The <b>AreAllAccessesGranted</b> function checks whether a set of requested access rights has been granted. The access rights are represented as bit flags in an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access mask</a>.


## -parameters




### -param GrantedAccess [in]

An access mask that specifies the access rights that have been granted.


### -param DesiredAccess [in]

An access mask that specifies the access rights that have been requested. This mask must have been mapped from generic to specific and standard access rights, usually by calling the 
<a href="https://msdn.microsoft.com/54b5cd73-4011-4dcf-a951-7350dbd6eeab">MapGenericMask</a> function.


## -returns



If all requested access rights have been granted, the return value is nonzero.

If not all requested access rights have been granted, the return value is zero.




## -remarks



The <b>AreAllAccessesGranted</b> function is commonly used by a server application to check the access rights of a client attempting to gain access to an object. When the bits set in the <i>DesiredAccess</i> parameter match the bits set in the <i>GrantedAccess</i> parameter, all requested rights have been granted.




## -see-also




<a href="https://msdn.microsoft.com/d9fd2e44-5782-40c9-a1cf-1788ca7afc50">AccessCheck</a>



<a href="https://msdn.microsoft.com/4bac6ebc-716a-4725-b9e6-a109b27dfc18">AreAnyAccessesGranted</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa375742(v=VS.85).aspx">Client/Server Access Control Functions</a>



<a href="https://msdn.microsoft.com/8301ed4f-9458-410b-af19-4f055656005a">Client/Server Access Control Overview</a>



<a href="https://msdn.microsoft.com/54b5cd73-4011-4dcf-a951-7350dbd6eeab">MapGenericMask</a>
 

 

