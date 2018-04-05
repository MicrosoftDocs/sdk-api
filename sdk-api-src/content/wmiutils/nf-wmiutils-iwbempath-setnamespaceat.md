---
UID: NF:wmiutils.IWbemPath.SetNamespaceAt
title: IWbemPath::SetNamespaceAt method
author: windows-driver-content
description: The IWbemPath::SetNamespace method sets a namespace in a path using zero-based indexing to designate where in the path the namespace is positioned.
old-location: wmi\iwbempath_setnamespaceat.htm
old-project: WmiSdk
ms.assetid: 59e8d4bc-1bf6-4fe7-a269-22f0317b876c
ms.author: windowsdriverdev
ms.date: 3/16/2018
ms.keywords: IWbemPath, IWbemPath interface [Windows Management Instrumentation], SetNamespaceAt method, IWbemPath::SetNamespaceAt, SetNamespaceAt method [Windows Management Instrumentation], SetNamespaceAt method [Windows Management Instrumentation], IWbemPath interface, SetNamespaceAt,IWbemPath.SetNamespaceAt, _hmm_iwbempath_setnamespaceat, wmi.iwbempath_setnamespaceat, wmiutils/IWbemPath::SetNamespaceAt
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: WMIQ_ASSOCQ_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wmiutils.dll
api_name:
-	IWbemPath.SetNamespaceAt
product: Windows
targetos: Windows
req.lib: Wbemuuid.lib
req.dll: Wmiutils.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWbemPath::SetNamespaceAt method


## -description


The <b>IWbemPath::SetNamespace</b> method sets a namespace in a path using zero-based indexing to designate where in the path the namespace is positioned.


## -parameters




### -param uIndex [in]

Index of where the namespace is to be put. The leftmost namespace in the path is index 0 (zero) with each namespace to the right having a progressively higher index value. The maximum permitted value is the current number of namespaces, because specifying that would add a namespace to the end as the namespaces have a zero-based index.


### -param pszName [in]

Namespace name.


## -returns



This method returns an <b>HRESULT</b> indicating the status of the method call.




## -see-also




<a href="https://msdn.microsoft.com/71b2597b-d82a-439d-b0b7-af76aefea6a2">IWbemPath</a>
 

 

