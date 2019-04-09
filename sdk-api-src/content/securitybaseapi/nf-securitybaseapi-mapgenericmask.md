---
UID: NF:securitybaseapi.MapGenericMask
title: MapGenericMask function (securitybaseapi.h)
author: windows-sdk-content
description: Maps the generic access rights in an access mask to specific and standard access rights. The function applies a mapping supplied in a GENERIC_MAPPING structure.
old-location: security\mapgenericmask.htm
tech.root: SecAuthZ
ms.assetid: 54b5cd73-4011-4dcf-a951-7350dbd6eeab
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MapGenericMask, MapGenericMask function [Security], _win32_mapgenericmask, security.mapgenericmask, securitybaseapi/MapGenericMask
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
 - API-MS-Win-DownLevel-AdvApi32-l1-1-1.dll
 - KernelBase.dll
 - API-MS-Win-Security-base-l1-1-0.dll
 - API-MS-Win-Security-base-l1-2-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Security-Base-L1-2-1.dll
api_name:
 - MapGenericMask
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MapGenericMask function


## -description


The <b>MapGenericMask</b> function maps the generic access rights in an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access mask</a> to specific and standard access rights. The function applies a mapping supplied in a 
<a href="https://msdn.microsoft.com/e3c49b47-9bc7-4000-a131-449345ebb9cd">GENERIC_MAPPING</a> structure.


## -parameters




### -param AccessMask [in, out]

A pointer to an access mask.


### -param GenericMapping [in]

A pointer to a 
<a href="https://msdn.microsoft.com/e3c49b47-9bc7-4000-a131-449345ebb9cd">GENERIC_MAPPING</a> structure specifying a mapping of generic access types to specific and standard access types.


## -returns



This function does not return a value.




## -remarks



After calling the <b>MapGenericMask</b> function, the access mask pointed to by the <i>AccessMask</i> parameter has none of its generic bits (GenericRead, GenericWrite, GenericExecute, or GenericAll) or undefined bits set, although it can have other bits set. If bits other than the generic bits are provided on input, this function does not clear them.


#### Examples

For an example that uses this function, see 
     <a href="https://msdn.microsoft.com/de21968e-4590-4798-9152-43204d55521f">Verifying Client Access with ACLs</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/d9fd2e44-5782-40c9-a1cf-1788ca7afc50">AccessCheck</a>



<a href="https://msdn.microsoft.com/91349693-8667-49dd-a813-657497b7d467">AreAllAccessesGranted</a>



<a href="https://msdn.microsoft.com/4bac6ebc-716a-4725-b9e6-a109b27dfc18">AreAnyAccessesGranted</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa375742(v=VS.85).aspx">Client/Server Access Control Functions</a>



<a href="https://msdn.microsoft.com/8301ed4f-9458-410b-af19-4f055656005a">Client/Server Access Control Overview</a>



<a href="https://msdn.microsoft.com/e3c49b47-9bc7-4000-a131-449345ebb9cd">GENERIC_MAPPING</a>
 

 

