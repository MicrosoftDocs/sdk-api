---
UID: NF:wbemcli.IWbemObjectAccess.ReadDWORD
title: IWbemObjectAccess::ReadDWORD
author: windows-driver-content
description: The ReadDWORD method reads 32 bits of property data using a property handle.
old-location: wmi\iwbemobjectaccess_readdword.htm
old-project: WmiSdk
ms.assetid: 5352dea3-6d10-42be-aa1e-786ace193827
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: IWbemObjectAccess interface [Windows Management Instrumentation],ReadDWORD method, IWbemObjectAccess.ReadDWORD, IWbemObjectAccess::ReadDWORD, ReadDWORD, ReadDWORD method [Windows Management Instrumentation], ReadDWORD method [Windows Management Instrumentation],IWbemObjectAccess interface, _hmm_iwbemobjectaccess_readdword, wbemcli/IWbemObjectAccess::ReadDWORD, wmi.iwbemobjectaccess_readdword
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
-	IWbemObjectAccess.ReadDWORD
product: Windows
targetos: Windows
req.lib: Wbemuuid.lib
req.dll: Esscli.dll; Fastprox.dll; Wbemess.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWbemObjectAccess::ReadDWORD


## -description


The <b>ReadDWORD</b> method reads 32 bits of property data using a property handle.


## -parameters




### -param lHandle [in]

Integer that contains the handle that identifies this property.


### -param pdw [out]

Pointer to a 32-bit unsigned integer used to return the data.


## -returns



This method returns an <b>HRESULT</b> that indicates the status of the method call. The following list lists the value contained withinan <b>HRESULT</b>.




## -see-also




<a href="https://msdn.microsoft.com/1025ae50-870f-4d38-8e83-3c6b628315c6">IWbemObjectAccess</a>
 

 

