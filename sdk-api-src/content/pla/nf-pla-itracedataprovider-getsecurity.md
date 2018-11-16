---
UID: NF:pla.ITraceDataProvider.GetSecurity
title: ITraceDataProvider::GetSecurity
author: windows-sdk-content
description: Retrieves the security information for the trace data provider.
old-location: pla\itracedataprovider_getsecurity.htm
tech.root: PLA
ms.assetid: 2f1618db-aa43-4cac-a652-db172781e988
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetSecurity, GetSecurity method [PLA], GetSecurity method [PLA],ITraceDataProvider interface, ITraceDataProvider interface [PLA],GetSecurity method, ITraceDataProvider.GetSecurity, ITraceDataProvider::GetSecurity, pla.itracedataprovider_getsecurity, pla/ITraceDataProvider::GetSecurity
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: pla.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: Pla.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Pla.dll
api_name:
 - ITraceDataProvider.GetSecurity
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- pla.h
: 
- ITraceDataProvider.GetSecurity
: 
---

# ITraceDataProvider::GetSecurity


## -description


Retrieves the security information for the trace data provider.


## -parameters




### -param SecurityInfo [in]

The object-related security information. For details, see the <a href="https://msdn.microsoft.com/e3e8b35d-9d18-4611-a898-72ca13e40d33">SECURITY_INFORMATION</a> data type.


### -param Sddl [out]

A string that describes the security descriptor for the object. For details, see <a href="https://msdn.microsoft.com/0a226629-084c-40c5-bdd4-ad7355c807cf">Security Descriptor Definition Language</a>.


## -returns



Returns S_OK if successful.




## -see-also




<a href="https://msdn.microsoft.com/bd2a49c1-8e18-4a14-a797-07f2b9c25812">ITraceDataProvider</a>



<a href="https://msdn.microsoft.com/07b6f5b3-5531-4174-9315-661695bd7c5d">ITraceDataProvider::SetSecurity</a>
 

 

