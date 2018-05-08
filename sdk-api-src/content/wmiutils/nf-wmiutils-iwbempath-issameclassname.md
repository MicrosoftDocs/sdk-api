---
UID: NF:wmiutils.IWbemPath.IsSameClassName
title: IWbemPath::IsSameClassName
author: windows-driver-content
description: The IWbemPath::IsSameClassName method tests whether the class name passed in matches the one in the path. The method can return TRUE only if the path actually has a class name.
old-location: wmi\iwbempath_issameclassname.htm
old-project: WmiSdk
ms.assetid: 7e0a907e-49d1-4775-885f-f059bb398804
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: IWbemPath interface [Windows Management Instrumentation],IsSameClassName method, IWbemPath.IsSameClassName, IWbemPath::IsSameClassName, IsSameClassName, IsSameClassName method [Windows Management Instrumentation], IsSameClassName method [Windows Management Instrumentation],IWbemPath interface, _hmm_iwbempath_issameclassname, wmi.iwbempath_issameclassname, wmiutils/IWbemPath::IsSameClassName
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
-	IWbemPath.IsSameClassName
product: Windows
targetos: Windows
req.lib: Wbemuuid.lib
req.dll: Wmiutils.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWbemPath::IsSameClassName


## -description


The 
<b>IWbemPath::IsSameClassName</b> method tests whether the class name passed in matches the one in the path. The method can return <b>TRUE</b> only if the path actually has a class name.


## -parameters




### -param wszClass [in]

Class name to test.


## -returns



This method returns a BOOL indicating whether the class name matches the one in the path.




## -see-also




<a href="https://msdn.microsoft.com/71b2597b-d82a-439d-b0b7-af76aefea6a2">IWbemPath</a>



<a href="https://msdn.microsoft.com/5b188426-9d7f-4e87-9eed-ce80e5d93c30">IWbemPathKeyList</a>
 

 

