---
UID: NF:wmiutils.IWbemPath.IsLocal
title: IWbemPath::IsLocal
author: windows-sdk-content
description: The IWbemPath::IsLocal method tests if the computer name passed in matches the computer name in the path, or if the server name in the path is NULL or &#0034;.&#0034;.
old-location: wmi\iwbempath_islocal.htm
tech.root: WmiSdk
ms.assetid: 28f33c70-095f-4bf0-98fa-29c5bb57f583
ms.author: windowssdkdev
ms.date: 08/28/2018
ms.keywords: IWbemPath interface [Windows Management Instrumentation],IsLocal method, IWbemPath.IsLocal, IWbemPath::IsLocal, IsLocal, IsLocal method [Windows Management Instrumentation], IsLocal method [Windows Management Instrumentation],IWbemPath interface, _hmm_iwbempath_islocal, wmi.iwbempath_islocal, wmiutils/IWbemPath::IsLocal
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
 - IWbemPath.IsLocal
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWbemPath::IsLocal


## -description


The 
<b>IWbemPath::IsLocal</b> method tests if the computer name passed in matches the computer name in the path, or if the server name in the path is <b>NULL</b> or ".".


## -parameters




### -param wszMachine [in]

Name of the computer to test.


## -returns



This method returns a <b>BOOL</b> indicating whether the path matches the passed in computer name, or if the server name in the path is <b>NULL</b> or ".".




## -see-also




<a href="https://msdn.microsoft.com/71b2597b-d82a-439d-b0b7-af76aefea6a2">IWbemPath</a>



<a href="https://msdn.microsoft.com/5b188426-9d7f-4e87-9eed-ce80e5d93c30">IWbemPathKeyList</a>
 

 

