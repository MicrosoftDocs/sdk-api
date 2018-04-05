---
UID: NF:wmiutils.IWbemPath.CreateClassPart
title: IWbemPath::CreateClassPart method
author: windows-driver-content
description: Initializes the class or key portion of the path.
old-location: wmi\iwbempath_createclasspart.htm
old-project: WmiSdk
ms.assetid: 6826bd2a-6036-4017-a58e-621fc2361031
ms.author: windowsdriverdev
ms.date: 3/16/2018
ms.keywords: CreateClassPart method [Windows Management Instrumentation], CreateClassPart method [Windows Management Instrumentation], IWbemPath interface, CreateClassPart,IWbemPath.CreateClassPart, IWbemPath, IWbemPath interface [Windows Management Instrumentation], CreateClassPart method, IWbemPath::CreateClassPart, _hmm_iwbempath_createclasspart, wmi.iwbempath_createclasspart, wmiutils/IWbemPath::CreateClassPart
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
-	IWbemPath.CreateClassPart
product: Windows
targetos: Windows
req.lib: Wbemuuid.lib
req.dll: Wmiutils.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWbemPath::CreateClassPart method


## -description


The 
<b>IWbemPath::CreateClassPart</b> method initializes the class or key portion of the path. This method is used when creating a path from scratch.


## -parameters




### -param lFlags [in]

Reserved. Must be 0 (zero).


### -param Name






#### - pszName [in]

Initial class name.


## -returns



This method returns an <b>HRESULT</b> indicating the status of the method call.




## -see-also




<a href="https://msdn.microsoft.com/71b2597b-d82a-439d-b0b7-af76aefea6a2">IWbemPath</a>
 

 

