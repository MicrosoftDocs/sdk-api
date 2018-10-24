---
UID: NF:wmiutils.IWbemPath.RemoveNamespaceAt
title: IWbemPath::RemoveNamespaceAt
author: windows-sdk-content
description: The IWbemPath::RemoveNamespaceAt method removes a namespace at a particular index. The leftmost namespace has an index value of 0 (zero), while namespaces to the right have progressively higher index values.
old-location: wmi\iwbempath_removenamespaceat.htm
tech.root: WmiSdk
ms.assetid: 425d26ee-c6f9-4562-9272-1c970fb6eb64
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: IWbemPath interface [Windows Management Instrumentation],RemoveNamespaceAt method, IWbemPath.RemoveNamespaceAt, IWbemPath::RemoveNamespaceAt, RemoveNamespaceAt, RemoveNamespaceAt method [Windows Management Instrumentation], RemoveNamespaceAt method [Windows Management Instrumentation],IWbemPath interface, _hmm_iwbempath_removenamespaceat, wmi.iwbempath_removenamespaceat, wmiutils/IWbemPath::RemoveNamespaceAt
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
 - IWbemPath.RemoveNamespaceAt
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWbemPath::RemoveNamespaceAt


## -description


The 
<b>IWbemPath::RemoveNamespaceAt</b> method removes a namespace at a particular index. The leftmost namespace has an index value of 0 (zero), while namespaces to the right have progressively higher index values.


## -parameters




### -param uIndex [in]

Zero-based index value of the namespace to be removed.


## -returns



This method returns an <b>HRESULT</b> with one of the following values.




## -see-also




<a href="https://msdn.microsoft.com/71b2597b-d82a-439d-b0b7-af76aefea6a2">IWbemPath</a>



<a href="https://msdn.microsoft.com/5b188426-9d7f-4e87-9eed-ce80e5d93c30">IWbemPathKeyList</a>
 

 

