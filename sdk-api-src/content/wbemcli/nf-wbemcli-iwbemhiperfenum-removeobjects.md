---
UID: NF:wbemcli.IWbemHiPerfEnum.RemoveObjects
title: IWbemHiPerfEnum::RemoveObjects
author: windows-sdk-content
description: The IWbemHiPerfEnum::RemoveObjects method removes objects (identified by their refresher identifiers) from a refresher.
old-location: wmi\iwbemhiperfenum_removeobjects.htm
tech.root: WmiSdk
ms.assetid: a4f25be2-8450-4e4c-ba6a-8d78c1fefca1
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWbemHiPerfEnum interface [Windows Management Instrumentation],RemoveObjects method, IWbemHiPerfEnum.RemoveObjects, IWbemHiPerfEnum::RemoveObjects, RemoveObjects, RemoveObjects method [Windows Management Instrumentation], RemoveObjects method [Windows Management Instrumentation],IWbemHiPerfEnum interface, _hmm_iwbemhiperfenum_removeobjects, wbemcli/IWbemHiPerfEnum::RemoveObjects, wmi.iwbemhiperfenum_removeobjects
ms.topic: method
req.header: wbemcli.h
req.include-header: Wbemidl.h
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wbemuuid.lib
 - Wbemuuid.dll
api_name:
 - IWbemHiPerfEnum.RemoveObjects
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWbemHiPerfEnum::RemoveObjects


## -description


The 
<b>IWbemHiPerfEnum::RemoveObjects</b> method removes objects (identified by their refresher identifiers) from a refresher.


## -parameters




### -param lFlags

Reserved. This parameter must be 0 (zero).


### -param uNumObjects [in]

Number of objects to remove.


### -param apIds [in]

Pointer to an array of integers that contains the refresher identifiers of the objects to remove.


## -returns



This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained withinan <b>HRESULT</b>.




## -see-also




<a href="https://msdn.microsoft.com/eb0d12c0-d746-4bae-b47d-50350d33447a">IWbemHiPerfEnum</a>
 

 

