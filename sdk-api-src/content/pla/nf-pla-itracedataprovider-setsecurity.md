---
UID: NF:pla.ITraceDataProvider.SetSecurity
title: ITraceDataProvider::SetSecurity (pla.h)
author: windows-sdk-content
description: Sets the security information for the trace data provider.
old-location: pla\itracedataprovider_setsecurity.htm
tech.root: PLA
ms.assetid: 07b6f5b3-5531-4174-9315-661695bd7c5d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITraceDataProvider interface [PLA],SetSecurity method, ITraceDataProvider.SetSecurity, ITraceDataProvider::SetSecurity, SetSecurity, SetSecurity method [PLA], SetSecurity method [PLA],ITraceDataProvider interface, pla.itracedataprovider_setsecurity, pla/ITraceDataProvider::SetSecurity
ms.topic: method
f1_keywords: 
 - "pla/ITraceDataProvider.SetSecurity"
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
 - ITraceDataProvider.SetSecurity
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITraceDataProvider::SetSecurity


## -description


Sets the security information for the trace data provider.


## -parameters




### -param Sddl [in]

A string that describes the security descriptor for the object. For details, see <a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/security-descriptor-string-format">Security Descriptor Definition Language</a>.


## -returns



Returns S_OK if successful.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nn-pla-itracedataprovider">ITraceDataProvider</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-itracedataprovider-getsecurity">ITraceDataProvider::GetSecurity</a>
 

 

