---
UID: NF:dsgetdc.DsGetDcCloseW
title: DsGetDcCloseW function (dsgetdc.h)
author: windows-sdk-content
description: Closes a domain controller enumeration operation.
old-location: ad\dsgetdcclose.htm
tech.root: ad
ms.assetid: d193e4cd-ad66-4d93-b912-348f17e93a6f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DsGetDcClose, DsGetDcClose function [Active Directory], DsGetDcCloseW, ad.dsgetdcclose, dsgetdc/DsGetDcClose, dsgetdc/DsGetDcCloseW
ms.topic: function
f1_keywords: 
 - "dsgetdc/DsGetDcClose"
req.header: dsgetdc.h
req.include-header: 
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
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
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
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DsGetDcCloseW function


## -description


The <b>DsGetDcClose</b>  function closes a domain controller enumeration operation.


## -parameters




### -param GetDcContextHandle [in]

Contains the domain controller enumeration context handle provided by the <a href="https://docs.microsoft.com/windows/desktop/api/dsgetdc/nf-dsgetdc-dsgetdcopena">DsGetDcOpen</a> function.


## -returns



This function does not return a value.




## -remarks



When this function is called, <i>GetDcContextHandle</i> is invalid and cannot be used.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/AD/directory-service-functions">Directory Service Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dsgetdc/nf-dsgetdc-dsgetdcopena">DsGetDcOpen</a>



<a href="https://docs.microsoft.com/windows/desktop/AD/enumerating-domain-controllers">Enumerating Domain Controllers</a>
 

 

