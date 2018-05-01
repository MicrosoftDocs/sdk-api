---
UID: NF:wbemcli.IWbemHiPerfEnum.AddObjects
title: IWbemHiPerfEnum::AddObjects method
author: windows-driver-content
description: The IWbemHiPerfEnum::AddObjects method adds the supplied instance objects to the enumerator.
old-location: wmi\iwbemhiperfenum_addobjects.htm
old-project: WmiSdk
ms.assetid: 6a6cd0f9-c6ed-4c9c-aa0f-7af2ac0fe73a
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: AddObjects method [Windows Management Instrumentation], AddObjects method [Windows Management Instrumentation], IWbemHiPerfEnum interface, AddObjects,IWbemHiPerfEnum.AddObjects, IWbemHiPerfEnum, IWbemHiPerfEnum interface [Windows Management Instrumentation], AddObjects method, IWbemHiPerfEnum::AddObjects, _hmm_iwbemhiperfenum_addobjects, wbemcli/IWbemHiPerfEnum::AddObjects, wmi.iwbemhiperfenum_addobjects
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: WMI_OBJ_TEXT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wbemuuid.lib
-	Wbemuuid.dll
api_name:
-	IWbemHiPerfEnum.AddObjects
product: Windows
targetos: Windows
req.lib: Wbemuuid.lib
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IWbemHiPerfEnum::AddObjects method


## -description


The <b>IWbemHiPerfEnum::AddObjects</b> method adds the supplied instance objects to the enumerator.


## -parameters




### -param lFlags

Reserved. This parameter must be 0.


### -param uNumObjects [in]

Number of items in the object and the number of identifiers in the parameter.


### -param apIds [in]

Pointer to an array of integers that contains a unique identifier for each object in the object array.


### -param apObj [in]

Pointer to an array of instance objects to add to the enumerator.


## -returns



This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained withinan <b>HRESULT</b>.




## -remarks



If an identifier already exists, <b>WBEM_E_FAILED</b> is returned. The refresher identifiers can be used to remove objects later.




## -see-also




<a href="https://msdn.microsoft.com/71ce1c89-446e-4137-9857-9d3c5921e0b7">IWbemHiPerfEnum</a>
 

 

