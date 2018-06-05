---
UID: NF:wcmconfig.ISettingsContext.Deserialize
title: ISettingsContext::Deserialize
author: windows-sdk-content
description: Deserializes the data in the stream that is provided to this context.
old-location: smi\isettingscontext_deserialize.htm
old-project: SMI
ms.assetid: 382f2864-047e-4095-929b-a8b67773eefb
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: Deserialize, Deserialize method [SMI], Deserialize method [SMI],ISettingsContext interface, ISettingsContext interface [SMI],Deserialize method, ISettingsContext.Deserialize, ISettingsContext::Deserialize, smi.isettingscontext_deserialize, wcmconfig/ISettingsContext::Deserialize
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WcmNamespaceAccess
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	SMIEngine.dll
api_name:
-	ISettingsContext.Deserialize
product: Windows
targetos: Windows
req.lib: 
req.dll: SMIEngine.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISettingsContext::Deserialize


## -description


Deserializes the data in the stream that is provided to this context.


## -parameters




### -param pStream [in]

A pointer to an IStream initialized stream object containing the XML representing a settings section of an answer (Unattend.xml) file.
An answers file is a file that facilitates the unattend process during setup or migration  to execute all of its tasks automatically, without user intervention.


### -param pTarget [in]

A pointer that identifies <a href="https://msdn.microsoft.com/f1dd3c93-43ca-4804-8330-55acaccf8ea8">ITargetInfo</a> target object that should be used while deserializing the stream. This target should match the target which will be used on the engine alongside this context.


### -param pppResults [out]

A pointer to an array of <a href="https://msdn.microsoft.com/0bbfd39a-0292-4d8e-ae31-f45aebd326a7">ISettingsResult</a> interface pointers. Each interface pointer identifies an issue which may have occurred during deserialization.




### -param pcResultCount [out]

The number of ISettingsResult objects in the array pppResults.


## -returns



This method returns an HRESULT value. <b>S_OK</b> indicates success. It returns <b>WCM_E_NAMESPACENOTFOUND</b> if pIdentity references a namespace that is not in the context.

This method may return <b>E_OUTOFMEMORY</b> if there are insufficient resources on the system to allocate the enumerators.




## -see-also




<a href="https://msdn.microsoft.com/29f43c3f-57bf-4208-a0bf-9b4414795a59">ISettingsContext</a>
 

 

