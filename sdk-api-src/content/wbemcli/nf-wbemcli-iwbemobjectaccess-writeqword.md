---
UID: NF:wbemcli.IWbemObjectAccess.WriteQWORD
title: IWbemObjectAccess::WriteQWORD method
author: windows-driver-content
description: The WriteQWORD method writes 64 bits of data to a property by using a property handle.
old-location: wmi\iwbemobjectaccess_writeqword.htm
old-project: WmiSdk
ms.assetid: f0d098b7-06f4-4a0a-8db9-fa1ef9be4468
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: IWbemObjectAccess, IWbemObjectAccess interface [Windows Management Instrumentation], WriteQWORD method, IWbemObjectAccess::WriteQWORD, WriteQWORD method [Windows Management Instrumentation], WriteQWORD method [Windows Management Instrumentation], IWbemObjectAccess interface, WriteQWORD,IWbemObjectAccess.WriteQWORD, _hmm_iwbemobjectaccess_writeqword, wbemcli/IWbemObjectAccess::WriteQWORD, wmi.iwbemobjectaccess_writeqword
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
-	Esscli.dll
-	Fastprox.dll
-	Wbemess.dll
api_name:
-	IWbemObjectAccess.WriteQWORD
product: Windows
targetos: Windows
req.lib: Wbemuuid.lib
req.dll: Esscli.dll; Fastprox.dll; Wbemess.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWbemObjectAccess::WriteQWORD method


## -description


The <b>WriteQWORD</b> method writes 64 bits of data to a property by using a property handle.


## -parameters




### -param lHandle [in]

Integer that contains the handle that identifies this property.


### -param pw [in]

Unsigned 64-bit integer that contains the data written to the specified property.


## -returns



This method returns <b>WBEM_S_NO_ERROR</b> if successful.




## -see-also




<a href="https://msdn.microsoft.com/1025ae50-870f-4d38-8e83-3c6b628315c6">IWbemObjectAccess</a>
 

 

