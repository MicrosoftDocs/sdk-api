---
UID: NF:wbemcli.IWbemObjectAccess.GetPropertyHandle
title: IWbemObjectAccess::GetPropertyHandle
author: windows-sdk-content
description: The GetPropertyHandle method returns a unique handle that identifies a property. You can use this handle to identify properties when using IWbemObjectAccess methods to read or write property values.
old-location: wmi\iwbemobjectaccess_getpropertyhandle.htm
old-project: WmiSdk
ms.assetid: 889d90cd-f53f-460e-b1c2-ed2b87863d58
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: GetPropertyHandle, GetPropertyHandle method [Windows Management Instrumentation], GetPropertyHandle method [Windows Management Instrumentation],IWbemObjectAccess interface, IWbemObjectAccess interface [Windows Management Instrumentation],GetPropertyHandle method, IWbemObjectAccess.GetPropertyHandle, IWbemObjectAccess::GetPropertyHandle, _hmm_iwbemobjectaccess_getpropertyhandle, wbemcli/IWbemObjectAccess::GetPropertyHandle, wmi.iwbemobjectaccess_getpropertyhandle
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Esscli.dll
-	Fastprox.dll
-	Wbemess.dll
api_name:
-	IWbemObjectAccess.GetPropertyHandle
product: Windows
targetos: Windows
req.lib: Wbemuuid.lib
req.dll: Esscli.dll; Fastprox.dll; Wbemess.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWbemObjectAccess::GetPropertyHandle


## -description


The 
<b>GetPropertyHandle</b> method returns a unique handle that identifies a property. You can use this handle to identify properties when using 
<a href="https://msdn.microsoft.com/1025ae50-870f-4d38-8e83-3c6b628315c6">IWbemObjectAccess</a> methods to read or write property values.


## -parameters




### -param wszPropertyName [in]

Constant, null-terminated string of 16-bit Unicode characters that contains the property name.


### -param pType [out]

Pointer to a <b>CIMTYPE</b> used to return the CIM type of the property.


### -param plHandle [out]

Pointer to an integer used to return the property handle.


## -returns



This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained withinan <b>HRESULT</b>.




## -remarks



Handles can be retrieved for all data types other than CIM_OBJECT and CIM_ARRAY. Returned handles work across all instances of a class.




## -see-also




<a href="https://msdn.microsoft.com/1025ae50-870f-4d38-8e83-3c6b628315c6">IWbemObjectAccess</a>
 

 

