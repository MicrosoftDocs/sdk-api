---
UID: NF:ntdsapi.DsFreeDomainControllerInfoA
title: DsFreeDomainControllerInfoA function
author: windows-sdk-content
description: The DsFreeDomainControllerInfo function frees memory that is allocated by DsGetDomainControllerInfo for data about the domain controllers in a domain.
old-location: ad\dsfreedomaincontrollerinfo.htm
tech.root: ad
ms.assetid: 1b6d3136-91e2-4653-a4b0-ae2f66a6c5a2
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: 1, 2, DsFreeDomainControllerInfo, DsFreeDomainControllerInfo function [Active Directory], DsFreeDomainControllerInfoA, DsFreeDomainControllerInfoW, _glines_dsfreedomaincontrollerinfo, ad.dsfreedomaincontrollerinfo, ntdsapi/DsFreeDomainControllerInfo, ntdsapi/DsFreeDomainControllerInfoA, ntdsapi/DsFreeDomainControllerInfoW
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
req.unicode-ansi: DsFreeDomainControllerInfoW (Unicode) and DsFreeDomainControllerInfoA (ANSI)
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
 - API-MS-Win-Security-ActiveDirectoryClient-l1-1-0.dll
 - KernelBase.dll
 - API-Ms-Win-Security-ActiveDirectoryClient-L1-1-1.dll
api_name:
 - DsFreeDomainControllerInfo
 - DsFreeDomainControllerInfoA
 - DsFreeDomainControllerInfoW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DsFreeDomainControllerInfoA function


## -description


The <b>DsFreeDomainControllerInfo</b> function frees memory that is allocated by 
<a href="https://msdn.microsoft.com/52db3b25-e6b0-4a0d-831b-89a203580cf1">DsGetDomainControllerInfo</a> for data about the domain controllers in a domain.


## -parameters




### -param InfoLevel [in]

Indicates what version of the <b>DS_DOMAIN_CONTROLLER_INFO</b> structure should be freed. This parameter can be one of the following values.



#### 1

The function frees the structure that contains  <a href="https://msdn.microsoft.com/6cc829ac-2aa6-49ef-b1ab-9c249249e0d6">DS_DOMAIN_CONTROLLER_INFO_1</a> data.



#### 2

The function frees the structure that contains <a href="https://msdn.microsoft.com/9d45b732-363d-4b20-ae5c-e9e76264bf1f">DS_DOMAIN_CONTROLLER_INFO_2</a> data.


### -param cInfo [in]

Indicates the number of items in <i>pInfo</i>.


### -param pInfo [in]

Pointer to an array of <a href="https://msdn.microsoft.com/6cc829ac-2aa6-49ef-b1ab-9c249249e0d6">DS_DOMAIN_CONTROLLER_INFO</a> structures to be freed.


## -returns



This function does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/6cc829ac-2aa6-49ef-b1ab-9c249249e0d6">DS_DOMAIN_CONTROLLER_INFO_1</a>



<a href="https://msdn.microsoft.com/a92783c2-ffb8-473e-8484-1c05ca5453ff">Domain Controller and Replication Management Functions</a>



<a href="https://msdn.microsoft.com/52db3b25-e6b0-4a0d-831b-89a203580cf1">DsGetDomainControllerInfo</a>
 

 

