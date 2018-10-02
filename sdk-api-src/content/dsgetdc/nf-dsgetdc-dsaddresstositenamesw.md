---
UID: NF:dsgetdc.DsAddressToSiteNamesW
title: DsAddressToSiteNamesW function
author: windows-sdk-content
description: Obtains the site names corresponding to the specified addresses.
old-location: ad\dsaddresstositenames.htm
tech.root: AD
ms.assetid: 4d70dbee-be33-4d2a-a200-3696443fa853
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: DsAddressToSiteNames, DsAddressToSiteNames function [Active Directory], DsAddressToSiteNamesA, DsAddressToSiteNamesW, _glines_dsaddresstositenames, ad.dsaddresstositenames, dsgetdc/DsAddressToSiteNames, dsgetdc/DsAddressToSiteNamesA, dsgetdc/DsAddressToSiteNamesW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: dsgetdc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DsAddressToSiteNamesW (Unicode) and DsAddressToSiteNamesA (ANSI)
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
 - DsAddressToSiteNames
 - DsAddressToSiteNamesA
 - DsAddressToSiteNamesW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DsAddressToSiteNamesW function


## -description


The <b>DsAddressToSiteNames</b> function obtains  the site names corresponding to the specified addresses.


## -parameters




### -param ComputerName [in, optional]

Pointer to a null-terminated string that specifies the name of the remote server to process this function. This parameter must be the name of a domain controller. A non-domain controller can call this function by calling 
<a href="https://msdn.microsoft.com/da8b2983-5e45-40b0-b552-c9b3a1d8ae94">DsGetDcName</a> to find the domain controller.


### -param EntryCount [in]

Contains the number of elements in the <i>SocketAddresses</i> array.


### -param SocketAddresses [in]

Contains an array of <a href="https://msdn.microsoft.com/37fbcb96-a859-4eca-8928-8051f95407b9">SOCKET_ADDRESS</a> structures that contain the addresses to convert. Each address in this array must be of the type <b>AF_INET</b>. <i>EntryCount</i> contains the number of elements in this array.


### -param SiteNames [out]

Receives an array of null-terminated string pointers that contain the site names for the addresses. Each element in this array corresponds to the same element in the <i>SocketAddresses</i> array. An element is <b>NULL</b> if the corresponding address does not map to any known site or if the address entry is not of the proper form. The caller must free this array when it is no longer required by calling <a href="https://msdn.microsoft.com/0e99483c-8cd7-402a-8bf6-1e0118764dd3">NetApiBufferFree</a>.


## -returns



Returns <b>NO_ERROR</b> if successful or a Win32 or RPC error otherwise. The following list lists possible error codes.




## -see-also




<a href="https://msdn.microsoft.com/7b519c81-5a6c-470a-a525-1894efd53305">Directory Service Functions</a>



<a href="https://msdn.microsoft.com/60ac6195-6e43-46da-a1e6-74ec989cd0c4">DsAddressToSiteNamesEx</a>



<a href="https://msdn.microsoft.com/da8b2983-5e45-40b0-b552-c9b3a1d8ae94">DsGetDcName</a>



<a href="https://msdn.microsoft.com/0e99483c-8cd7-402a-8bf6-1e0118764dd3">NetApiBufferFree</a>
 

 

