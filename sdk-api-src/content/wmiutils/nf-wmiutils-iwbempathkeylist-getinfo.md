---
UID: NF:wmiutils.IWbemPathKeyList.GetInfo
title: IWbemPathKeyList::GetInfo (wmiutils.h)
author: windows-sdk-content
description: The IWbemPathKeyList::GetInfo method retrieves the status bits for the key.
old-location: wmi\iwbempathkeylist_getinfo.htm
tech.root: WmiSdk
ms.assetid: e5df2222-988c-4f61-9b1a-9bccb647826d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetInfo, GetInfo method [Windows Management Instrumentation], GetInfo method [Windows Management Instrumentation],IWbemPathKeyList interface, IWbemPathKeyList interface [Windows Management Instrumentation],GetInfo method, IWbemPathKeyList.GetInfo, IWbemPathKeyList::GetInfo, WBEMPATH_INFO_CONTAINS_SINGLETON, WBEMPATH_INFO_HAS_IMPLIED_KEY, WBEMPATH_INFO_HAS_V2_REF_PATHS, WBEMPATH_INFO_IS_COMPOUND, _hmm_iwbempathkeylist_getinfo, wmi.iwbempathkeylist_getinfo, wmiutils/IWbemPathKeyList::GetInfo
ms.topic: method
f1_keywords: 
 - "wmiutils/IWbemPathKeyList.GetInfo"
dev_langs:
 - c++
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
 - IWbemPathKeyList.GetInfo
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/windows/desktop/api/wmiutils/nn-wmiutils-iwbempath">IWbemPath</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmiutils/nn-wmiutils-iwbempathkeylist">IWbemPathKeyList</a>
 

 

