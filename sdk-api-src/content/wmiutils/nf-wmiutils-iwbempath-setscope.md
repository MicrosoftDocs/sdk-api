---
UID: NF:wmiutils.IWbemPath.SetScope
title: IWbemPath::SetScope
author: windows-sdk-content
description: The IWbemPath::SetScope method sets a scope in the path based upon an index. The index is always 0 (zero) and the scope is the class or key portion of the path. This method also sets the class name.
old-location: wmi\iwbempath_setscope.htm
old-project: WmiSdk
ms.assetid: 0b4597ec-0d08-4929-9591-21588ded66bb
ms.author: windowssdkdev
ms.date: 08/28/2018
ms.keywords: IWbemPath interface [Windows Management Instrumentation],SetScope method, IWbemPath.SetScope, IWbemPath::SetScope, SetScope, SetScope method [Windows Management Instrumentation], SetScope method [Windows Management Instrumentation],IWbemPath interface, _hmm_iwbempath_setscope, wmi.iwbempath_setscope, wmiutils/IWbemPath::SetScope
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wmiutils.h
req.include-header: 
req.redist: 
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmiutils.dll
api_name:
 - IWbemPath.SetScope
product: Windows
targetos: Windows
req.lib: Wbemuuid.lib
req.dll: Wmiutils.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWbemPath::SetScope


## -description


The 
<b>IWbemPath::SetScope</b> method sets a scope in the path based upon an index. The index is always 0  (zero) and the scope is the class or key portion of the path. This method also sets the class name.


## -parameters




### -param uIndex [in]

Index of the scope.


### -param pszClass [in]

Class name of the scope.


## -returns



This method returns an <b>HRESULT</b> indicating the status of the method call.




## -see-also




<a href="https://msdn.microsoft.com/71b2597b-d82a-439d-b0b7-af76aefea6a2">IWbemPath</a>
 

 

