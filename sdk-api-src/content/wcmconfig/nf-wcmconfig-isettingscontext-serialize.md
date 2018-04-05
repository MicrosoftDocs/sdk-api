---
UID: NF:wcmconfig.ISettingsContext.Serialize
title: ISettingsContext::Serialize method
author: windows-driver-content
description: Serializes the data in this context into the provided stream.
old-location: smi\isettingscontext_serialize.htm
old-project: SMI
ms.assetid: 13b29096-8572-4539-abd4-de22a9594f38
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: ISettingsContext, ISettingsContext interface [SMI], Serialize method, ISettingsContext::Serialize, Serialize method [SMI], Serialize method [SMI], ISettingsContext interface, Serialize,ISettingsContext.Serialize, smi.isettingscontext_serialize, wcmconfig/ISettingsContext::Serialize
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wcmconfig.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WcmConfig.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WcmNamespaceAccess
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	SMIEngine.dll
api_name:
-	ISettingsContext.Serialize
product: Windows
targetos: Windows
req.lib: 
req.dll: SMIEngine.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISettingsContext::Serialize method


## -description


Serializes the data in this context into the provided stream.


## -parameters




### -param pStream [in]

The stream into which the XML, produced by the method, is inserted.


### -param pTarget [in]

Defines the parameters of the image against which the context must be serialized. This should match the target used while constructing the context.


## -returns



This method returns an HRESULT value. <b>S_OK</b> indicates success.




## -see-also




<a href="https://msdn.microsoft.com/29f43c3f-57bf-4208-a0bf-9b4414795a59">ISettingsContext</a>
 

 

