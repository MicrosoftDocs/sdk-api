---
UID: NF:wmiutils.IWbemPathKeyList.GetInfo
title: IWbemPathKeyList::GetInfo
author: windows-driver-content
description: The IWbemPathKeyList::GetInfo method retrieves the status bits for the key.
old-location: wmi\iwbempathkeylist_getinfo.htm
old-project: WmiSdk
ms.assetid: e5df2222-988c-4f61-9b1a-9bccb647826d
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: GetInfo, GetInfo method [Windows Management Instrumentation], GetInfo method [Windows Management Instrumentation],IWbemPathKeyList interface, IWbemPathKeyList interface [Windows Management Instrumentation],GetInfo method, IWbemPathKeyList.GetInfo, IWbemPathKeyList::GetInfo, WBEMPATH_INFO_CONTAINS_SINGLETON, WBEMPATH_INFO_HAS_IMPLIED_KEY, WBEMPATH_INFO_HAS_V2_REF_PATHS, WBEMPATH_INFO_IS_COMPOUND, _hmm_iwbempathkeylist_getinfo, wmi.iwbempathkeylist_getinfo, wmiutils/IWbemPathKeyList::GetInfo
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
-	IWbemPathKeyList.GetInfo
product: Windows
targetos: Windows
req.lib: Wbemuuid.lib
req.dll: Wmiutils.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWbemPathKeyList::GetInfo


## -description


The 
<b>IWbemPathKeyList::GetInfo</b> method retrieves the status bits for the key.


## -parameters




### -param uRequestedInfo [in]

Reserved. Must be 0 (zero).


### -param puResponse [out]

Status for the key. The following bits indicate the values available.



#### WBEMPATH_INFO_IS_COMPOUND

Compound key is used.



#### WBEMPATH_INFO_HAS_V2_REF_PATHS

One or more of the keys has a CIM_REFERENCE.



#### WBEMPATH_INFO_HAS_IMPLIED_KEY

Key names are missing somewhere.



#### WBEMPATH_INFO_CONTAINS_SINGLETON

One or more singletons in the path.


## -returns



This method returns an <b>HRESULT</b> indicating the status of the method call.




## -see-also




<a href="https://msdn.microsoft.com/71b2597b-d82a-439d-b0b7-af76aefea6a2">IWbemPath</a>



<a href="https://msdn.microsoft.com/5b188426-9d7f-4e87-9eed-ce80e5d93c30">IWbemPathKeyList</a>
 

 

