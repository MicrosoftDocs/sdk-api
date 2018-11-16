---
UID: NS:nspapi._SERVICE_ADDRESSES
title: "_SERVICE_ADDRESSES"
author: windows-sdk-content
description: The SERVICE_ADDRESSES structure contains an array of SERVICE_ADDRESS data structures.
old-location: winsock\service_addresses_2.htm
tech.root: WinSock
ms.assetid: 1ed0c634-4f09-49c1-8fbf-9182d6a4bd51
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: "*LPSERVICE_ADDRESSES, *PSERVICE_ADDRESSES, SERVICE_ADDRESSES, SERVICE_ADDRESSES structure [Winsock], _SERVICE_ADDRESSES, _win32_service_addresses_2, nspapi/SERVICE_ADDRESSES, winsock.service_addresses_2"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: nspapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Nspapi.h
api_name:
 - SERVICE_ADDRESSES
product: Windows
targetos: Windows
req.typenames: SERVICE_ADDRESSES, *PSERVICE_ADDRESSES, *LPSERVICE_ADDRESSES
req.redist: 
---

# _SERVICE_ADDRESSES structure


## -description


The 
<b>SERVICE_ADDRESSES</b> structure contains an array of 
<a href="https://msdn.microsoft.com/5fc99e3a-7316-4950-9249-968bbc4168c2">SERVICE_ADDRESS</a> data structures.


## -struct-fields




### -field dwAddressCount

Number of 
<a href="https://msdn.microsoft.com/5fc99e3a-7316-4950-9249-968bbc4168c2">SERVICE_ADDRESS</a> structures in the <b>Addresses</b> array.


### -field Addressses

 


### -field Addressses.size_is

 


### -field Addressses.size_is.dwAddressCount

 


### -field Addresses

Array of 
<a href="https://msdn.microsoft.com/5fc99e3a-7316-4950-9249-968bbc4168c2">SERVICE_ADDRESS</a> data structures. Each 
<b>SERVICE_ADDRESS</b> structure contains information about a network service address.


## -see-also




<a href="https://msdn.microsoft.com/5fc99e3a-7316-4950-9249-968bbc4168c2">SERVICE_ADDRESS</a>



<a href="https://msdn.microsoft.com/e76e0c1b-8cbf-45ad-a685-fb672801c24d">SERVICE_INFO</a>
 

 

