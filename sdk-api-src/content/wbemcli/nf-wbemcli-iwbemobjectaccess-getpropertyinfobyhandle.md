---
UID: NF:wbemcli.IWbemObjectAccess.GetPropertyInfoByHandle
title: IWbemObjectAccess::GetPropertyInfoByHandle
author: windows-sdk-content
description: The GetPropertyInfoByHandle method returns the name and data type of the property that is associated with a property handle.
old-location: wmi\iwbemobjectaccess_getpropertyinfobyhandle.htm
tech.root: WmiSdk
ms.assetid: a29157a8-50da-485d-a2b1-bf9645ba9963
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: GetPropertyInfoByHandle, GetPropertyInfoByHandle method [Windows Management Instrumentation], GetPropertyInfoByHandle method [Windows Management Instrumentation],IWbemObjectAccess interface, IWbemObjectAccess interface [Windows Management Instrumentation],GetPropertyInfoByHandle method, IWbemObjectAccess.GetPropertyInfoByHandle, IWbemObjectAccess::GetPropertyInfoByHandle, _hmm_iwbemobjectaccess_getpropertyinfobyhandle, wbemcli/IWbemObjectAccess::GetPropertyInfoByHandle, wmi.iwbemobjectaccess_getpropertyinfobyhandle
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
req.lib: Wbemuuid.lib
req.dll: Esscli.dll; Fastprox.dll; Wbemess.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Esscli.dll
 - Fastprox.dll
 - Wbemess.dll
api_name:
 - IWbemObjectAccess.GetPropertyInfoByHandle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWbemObjectAccess::GetPropertyInfoByHandle


## -description


The 
<b>GetPropertyInfoByHandle</b> method returns the name and data type of the property that is associated with a property handle.


## -parameters




### -param lHandle [in]

Integer that contains the handle identifying the property.


### -param pstrName [out]

Pointer to a string used to return the name of the specified property.


### -param pType [out]

Pointer to a <b>CIMTYPE</b> used to return the type of the property.


## -returns



This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained withinan <b>HRESULT</b>.




## -see-also




<a href="https://msdn.microsoft.com/1025ae50-870f-4d38-8e83-3c6b628315c6">IWbemObjectAccess</a>
 

 

