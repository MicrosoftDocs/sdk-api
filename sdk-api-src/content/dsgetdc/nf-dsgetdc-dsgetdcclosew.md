---
UID: NF:dsgetdc.DsGetDcCloseW
title: DsGetDcCloseW function
author: windows-sdk-content
description: Closes a domain controller enumeration operation.
old-location: ad\dsgetdcclose.htm
old-project: ad
ms.assetid: d193e4cd-ad66-4d93-b912-348f17e93a6f
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DsGetDcClose, DsGetDcClose function [Active Directory], DsGetDcCloseW, ad.dsgetdcclose, dsgetdc/DsGetDcClose, dsgetdc/DsGetDcCloseW
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
req.unicode-ansi: DsGetDcCloseW (Unicode)
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
 - DsGetDcClose
 - DsGetDcCloseW
product: Windows
targetos: Windows
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
---

# DsGetDcCloseW function


## -description


The <b>DsGetDcClose</b>  function closes a domain controller enumeration operation.


## -parameters




### -param GetDcContextHandle [in]

Contains the domain controller enumeration context handle provided by the <a href="https://msdn.microsoft.com/2811cc30-f367-4f1a-8f0c-ed0a77dad24c">DsGetDcOpen</a> function.


## -returns



This function does not return a value.




## -remarks



When this function is called, <i>GetDcContextHandle</i> is invalid and cannot be used.




## -see-also




<a href="https://msdn.microsoft.com/7b519c81-5a6c-470a-a525-1894efd53305">Directory Service Functions</a>



<a href="https://msdn.microsoft.com/2811cc30-f367-4f1a-8f0c-ed0a77dad24c">DsGetDcOpen</a>



<a href="https://msdn.microsoft.com/bfc92777-6944-406a-8b93-949a1cf3e2c3">Enumerating Domain Controllers</a>
 

 

