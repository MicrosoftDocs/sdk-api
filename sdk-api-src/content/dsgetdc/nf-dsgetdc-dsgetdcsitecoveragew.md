---
UID: NF:dsgetdc.DsGetDcSiteCoverageW
title: DsGetDcSiteCoverageW function
author: windows-sdk-content
description: The DsGetDcSiteCoverage function returns the site names of all sites covered by a domain controller.
old-location: ad\dsgetdcsitecoverage.htm
old-project: ad
ms.assetid: e0f757d9-36b6-40f8-a1db-fb5b9862b46a
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DsGetDcSiteCoverage, DsGetDcSiteCoverage function [Active Directory], DsGetDcSiteCoverageA, DsGetDcSiteCoverageW, _glines_dsgetdcsitecoverage, ad.dsgetdcsitecoverage, dsgetdc/DsGetDcSiteCoverage, dsgetdc/DsGetDcSiteCoverageA, dsgetdc/DsGetDcSiteCoverageW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: dsgetdc.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DsGetDcSiteCoverageW (Unicode) and DsGetDcSiteCoverageA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: DSDISPLAYSPECOPTIONS, *PDSDISPLAYSPECOPTIONS, *LPDSDISPLAYSPECOPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netapi32.dll
api_name:
 - DsGetDcSiteCoverage
 - DsGetDcSiteCoverageA
 - DsGetDcSiteCoverageW
product: Windows
targetos: Windows
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
---

# DsGetDcSiteCoverageW function


## -description


The <b>DsGetDcSiteCoverage</b> function returns the site names of all sites covered by a domain controller.


## -parameters




### -param ServerName [in, optional]

The null-terminated string value that specifies the name of the remote domain controller.


### -param EntryCount [out]

Pointer to a <b>ULONG</b> value that receives  the number of sites covered by the domain controller.


### -param SiteNames [out]

Pointer to an array of pointers to null-terminated strings that receives the site names. To free the returned buffer, call the <a href="https://msdn.microsoft.com/0e99483c-8cd7-402a-8bf6-1e0118764dd3">NetApiBufferFree</a> function.


## -returns



This function returns DSGETDCAPI DWORD __stdcall.




## -see-also




<a href="https://msdn.microsoft.com/7b519c81-5a6c-470a-a525-1894efd53305">Directory Service Functions</a>



<a href="https://msdn.microsoft.com/2dfffd9a-af4f-4a93-8b3c-966e4f7c455f">DsGetSiteName</a>



<a href="https://msdn.microsoft.com/0e99483c-8cd7-402a-8bf6-1e0118764dd3">NetApiBufferFree</a>
 

 

