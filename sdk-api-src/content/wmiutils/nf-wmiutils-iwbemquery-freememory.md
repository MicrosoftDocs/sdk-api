---
UID: NF:wmiutils.IWbemQuery.FreeMemory
title: IWbemQuery::FreeMemory (wmiutils.h)
author: windows-sdk-content
description: The IWbemQuery::FreeMemory method frees the memory that the parser returns to a caller in a previous call to GetAnalysis.
old-location: wmi\iwbemquery_freememory.htm
tech.root: WmiSdk
ms.assetid: fbc4329d-73b8-4104-b3e0-e6dc12938b4f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FreeMemory, FreeMemory method [Windows Management Instrumentation], FreeMemory method [Windows Management Instrumentation],IWbemQuery interface, IWbemQuery interface [Windows Management Instrumentation],FreeMemory method, IWbemQuery.FreeMemory, IWbemQuery::FreeMemory, _hmm_iwbemquery_freememory, wmi.iwbemquery_freememory, wmiutils/IWbemQuery::FreeMemory
ms.topic: method
req.header: wmiutils.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wbemuuid.lib
req.dll: Wmiutils.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmiutils.dll
api_name:
 - IWbemQuery.FreeMemory
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWbemQuery::FreeMemory


## -description


The <b>IWbemQuery::FreeMemory</b> method frees the memory that the parser returns to  a caller in a previous call to 
<a href="https://msdn.microsoft.com/06cd2593-58f5-46b9-9100-debad0280d90">GetAnalysis</a>.


## -parameters




### -param pMem [in]

Pointer to the memory to be freed.


## -returns



This method returns an <b>HRESULT</b> indicating the status of the method call.




## -see-also




<a href="https://msdn.microsoft.com/4a0c0c1d-3d84-491f-8379-d164821fa71b">IWbemQuery</a>
 

 

