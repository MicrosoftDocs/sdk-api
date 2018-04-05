---
UID: NF:wcmconfig.ISettingsItem.GetName
title: ISettingsItem::GetName method
author: windows-driver-content
description: Gets the name of the item.
old-location: smi\isettingsitem_getname.htm
old-project: SMI
ms.assetid: a8517c53-5833-4087-91eb-3eb9301e0d3a
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GetName method [SMI], GetName method [SMI], ISettingsItem interface, GetName,ISettingsItem.GetName, ISettingsItem, ISettingsItem interface [SMI], GetName method, ISettingsItem::GetName, smi.isettingsitem_getname, wcmconfig/ISettingsItem::GetName
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
-	ISettingsItem.GetName
product: Windows
targetos: Windows
req.lib: 
req.dll: SMIEngine.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISettingsItem::GetName method


## -description


Gets the name of the item.


## -parameters




### -param Name [out]

The name of the item.


## -returns



This method returns an HRESULT value. <b>S_OK</b> indicates success. It may return <b>E_OUTOFMEMORY</b> if there are insufficient resources to allocate Name. 




## -see-also




<a href="https://msdn.microsoft.com/a743d942-69f9-426b-be88-adf88b9bb1e0">ISettingsItem</a>
 

 

