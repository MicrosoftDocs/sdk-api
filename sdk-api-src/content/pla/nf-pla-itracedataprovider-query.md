---
UID: NF:pla.ITraceDataProvider.Query
title: ITraceDataProvider::Query
author: windows-sdk-content
description: Retrieves details about a registered provider.
old-location: pla\itracedataprovider_query.htm
tech.root: PLA
ms.assetid: b3d1720f-3a74-4040-803b-266bd0d50cfc
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ITraceDataProvider interface [PLA],Query method, ITraceDataProvider.Query, ITraceDataProvider::Query, Query, Query method [PLA], Query method [PLA],ITraceDataProvider interface, base.itracedataprovider_query, pla.itracedataprovider_query, pla/ITraceDataProvider::Query
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
 - ITraceDataProvider.Query
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
- ITraceDataProvider.Query
: 
---

# ITraceDataProvider::Query


## -description


Retrieves details about a registered provider.


## -parameters




### -param bstrName [in]

The name of the registered provider. The name is case-insensitive. You can also specify the string form of the provider's GUID.


### -param bstrServer [in]

The computer on which the provider is registered. You can specify the computer's name, fully qualified domain name, or IP address.


## -returns



Returns S_OK if successful.




## -remarks



To specify kernel providers, set the <i>bstrName</i> parameter to "Windows Kernel Trace".

To specify the context logger, set <i>bstrName</i> to "Circular Kernel Context Logger". The context logger provides a snapshot of the current state of the computer. The logger writes to an in-memory 100-megabyte circular log (not to a file). To release its contents to consumers, call the <a href="https://msdn.microsoft.com/7e432e1f-4b86-45dc-93d5-df603068273d">IDataCollectorSet::Commit</a> method to flush the session.




## -see-also




<a href="https://msdn.microsoft.com/bd2a49c1-8e18-4a14-a797-07f2b9c25812">ITraceDataProvider</a>
 

 

