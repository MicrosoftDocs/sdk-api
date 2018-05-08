---
UID: NF:wcmconfig.ISettingsItem.GetPath
title: ISettingsItem::GetPath
author: windows-driver-content
description: Gets the path for the item.
old-location: smi\isettingsitem_getpath.htm
old-project: SMI
ms.assetid: 221b5929-7300-4d01-b93e-7c82c446f52b
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GetPath, GetPath method [SMI], GetPath method [SMI],ISettingsItem interface, ISettingsItem interface [SMI],GetPath method, ISettingsItem.GetPath, ISettingsItem::GetPath, smi.isettingsitem_getpath, wcmconfig/ISettingsItem::GetPath
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
-	ISettingsItem.GetPath
product: Windows
targetos: Windows
req.lib: 
req.dll: SMIEngine.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISettingsItem::GetPath


## -description


Gets the path for the item.


## -parameters




### -param Path [out]

The path to the current setting. This path should be handled as opaque, and should be used only for invocations of <a href="https://msdn.microsoft.com/8b51329e-dc81-46dc-b174-0191e2eea44a">CreateSettingByPath</a>, <a href="https://msdn.microsoft.com/a4270c46-b214-4232-b414-d6b6e4e35635">GetSettingByPath</a>, or <a href="https://msdn.microsoft.com/5613df85-009f-4aab-91bc-797a6cf73cd0">RemoveSettingByPath</a>.


## -returns



This method returns an HRESULT value. <b>S_OK</b> indicates success. It may return <b>E_OUTOFMEMORY</b> if there are insufficient resources.




## -see-also




<a href="https://msdn.microsoft.com/a743d942-69f9-426b-be88-adf88b9bb1e0">ISettingsItem</a>
 

 

