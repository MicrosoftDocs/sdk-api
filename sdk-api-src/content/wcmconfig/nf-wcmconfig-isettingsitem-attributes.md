---
UID: NF:wcmconfig.ISettingsItem.Attributes
title: ISettingsItem::Attributes
author: windows-sdk-content
description: Gets the dictionary of attributes.
old-location: smi\isettingsitem_attributes.htm
old-project: smi
ms.assetid: 7a6751f2-0934-4329-9ab2-9ae9802bc33e
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: Attributes, Attributes method [SMI], Attributes method [SMI],ISettingsItem interface, ISettingsItem interface [SMI],Attributes method, ISettingsItem.Attributes, ISettingsItem::Attributes, smi.isettingsitem_attributes, wcmconfig/ISettingsItem::Attributes
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SMIEngine.dll
api_name:
 - ISettingsItem.Attributes
product: Windows
targetos: Windows
req.lib: 
req.dll: SMIEngine.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISettingsItem::Attributes


## -description


Gets the dictionary of attributes.


## -parameters




### -param Attributes [out]

A pointer to an  <a href="https://msdn.microsoft.com/f43245f1-81d9-4b06-8f0c-d490618a99fa">IItemEnumerator</a> object that represents the dictionary of attributes.


## -returns



This method returns an HRESULT value. <b>S_OK</b> indicates success. It may return <b>E_OUTOFMEMORY</b> if there are insufficient resources to allocate attributes.




## -see-also




<a href="https://msdn.microsoft.com/a743d942-69f9-426b-be88-adf88b9bb1e0">ISettingsItem</a>
 

 

