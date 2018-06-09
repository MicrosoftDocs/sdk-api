---
UID: NF:wbemcli.IWbemHiPerfEnum.GetObjects
title: IWbemHiPerfEnum::GetObjects
author: windows-sdk-content
description: The IWbemHiPerfEnum::GetObjects method retrieves objects currently residing in the enumerator.
old-location: wmi\iwbemhiperfenum_getobjects.htm
old-project: WmiSdk
ms.assetid: 27dd9c2c-236e-41be-bfaa-90ebf8dfb1bc
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: GetObjects, GetObjects method [Windows Management Instrumentation], GetObjects method [Windows Management Instrumentation],IWbemHiPerfEnum interface, IWbemHiPerfEnum interface [Windows Management Instrumentation],GetObjects method, IWbemHiPerfEnum.GetObjects, IWbemHiPerfEnum::GetObjects, _hmm_iwbemhiperfenum_getobjects, wbemcli/IWbemHiPerfEnum::GetObjects, wmi.iwbemhiperfenum_getobjects
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WMI_OBJ_TEXT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wbemuuid.lib
 - Wbemuuid.dll
api_name:
 - IWbemHiPerfEnum.GetObjects
product: Windows
targetos: Windows
req.lib: Wbemuuid.lib
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IWbemHiPerfEnum::GetObjects


## -description


The 
<b>IWbemHiPerfEnum::GetObjects</b> method retrieves objects currently residing in the enumerator.


## -parameters




### -param lFlags [in]

Integer that contains the flags.


### -param uNumObjects [in]

Size of the array passed to this method in the <i>apObj</i> parameter.


### -param apObj [out]

Pointer that holds the reference to an array of 
<a href="https://msdn.microsoft.com/1025ae50-870f-4d38-8e83-3c6b628315c6">IWbemObjectAccess</a> objects, which contains the returned objects. The array must be big enough to hold all objects in the enumerator.


### -param puReturned [out]

Pointer to a <b>ULONG</b> used to return the number of objects placed in the array.


## -returns



This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.




## -remarks



The array must be large enough to hold all objects, or <i>puReturned</i> is filled with the number of returned objects, and <b>WBEM_E_BUFFER_TOO_SMALL</b> is returned.




## -see-also




<a href="https://msdn.microsoft.com/eb0d12c0-d746-4bae-b47d-50350d33447a">IWbemHiPerfEnum</a>
 

 

