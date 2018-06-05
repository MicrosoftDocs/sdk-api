---
UID: NF:wmiutils.IWbemPathKeyList.MakeSingleton
title: IWbemPathKeyList::MakeSingleton
author: windows-sdk-content
description: The IWbemPathKeyList::MakeSingleton method governs whether or not a key is singleton.
old-location: wmi\iwbempathkeylist_makesingleton.htm
old-project: WmiSdk
ms.assetid: 6dd7fd31-126c-4702-8e43-3e6b08912b30
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: IWbemPathKeyList interface [Windows Management Instrumentation],MakeSingleton method, IWbemPathKeyList.MakeSingleton, IWbemPathKeyList::MakeSingleton, MakeSingleton, MakeSingleton method [Windows Management Instrumentation], MakeSingleton method [Windows Management Instrumentation],IWbemPathKeyList interface, _hmm_iwbempathkeylist_makesingleton, wmi.iwbempathkeylist_makesingleton, wmiutils/IWbemPathKeyList::MakeSingleton
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WMIQ_ASSOCQ_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wmiutils.dll
api_name:
-	IWbemPathKeyList.MakeSingleton
product: Windows
targetos: Windows
req.lib: Wbemuuid.lib
req.dll: Wmiutils.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWbemPathKeyList::MakeSingleton


## -description


The 
<b>IWbemPathKeyList::MakeSingleton</b> method governs whether or not a key is singleton.


## -parameters




### -param bSet [in]

If <b>TRUE</b>, the key becomes singleton. If <b>FALSE</b>, the key is no longer singleton.


## -returns



This method returns an <b>HRESULT</b> indicating the status of the method call.




## -see-also




<a href="https://msdn.microsoft.com/71b2597b-d82a-439d-b0b7-af76aefea6a2">IWbemPath</a>



<a href="https://msdn.microsoft.com/5b188426-9d7f-4e87-9eed-ce80e5d93c30">IWbemPathKeyList</a>
 

 

