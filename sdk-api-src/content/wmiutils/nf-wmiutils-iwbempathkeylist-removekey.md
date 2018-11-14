---
UID: NF:wmiutils.IWbemPathKeyList.RemoveKey
title: IWbemPathKeyList::RemoveKey
author: windows-sdk-content
description: The IWbemPathKeyList::RemoveKey method removes the key that matches the wszName parameter.
old-location: wmi\iwbempathkeylist_removekey.htm
tech.root: WmiSdk
ms.assetid: 07166023-2945-49d5-9d2d-8cac12053ed9
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: IWbemPathKeyList interface [Windows Management Instrumentation],RemoveKey method, IWbemPathKeyList.RemoveKey, IWbemPathKeyList::RemoveKey, RemoveKey, RemoveKey method [Windows Management Instrumentation], RemoveKey method [Windows Management Instrumentation],IWbemPathKeyList interface, _hmm_iwbempathkeylist_removekey, wmi.iwbempathkeylist_removekey, wmiutils/IWbemPathKeyList::RemoveKey
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
 - IWbemPathKeyList.RemoveKey
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- wmiutils.h
: 
- IWbemPathKeyList.RemoveKey
: 
---

# IWbemPathKeyList::RemoveKey


## -description


The 
<b>IWbemPathKeyList::RemoveKey</b> method removes the key that matches the <i>wszName</i> parameter.


## -parameters




### -param wszName [in, out]

Name of the key to be removed.


### -param uFlags [in]

Reserved. Must be 0 (zero).


## -returns



This method returns an <b>HRESULT</b> indicating the status of the method call.




## -see-also




<a href="https://msdn.microsoft.com/71b2597b-d82a-439d-b0b7-af76aefea6a2">IWbemPath</a>



<a href="https://msdn.microsoft.com/5b188426-9d7f-4e87-9eed-ce80e5d93c30">IWbemPathKeyList</a>



<a href="https://msdn.microsoft.com/57c36ecd-7a24-4055-b373-9193fd945363">IWbemPathKeyList::RemoveAllKeys</a>
 

 

