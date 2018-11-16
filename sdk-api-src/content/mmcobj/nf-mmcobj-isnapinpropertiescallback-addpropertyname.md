---
UID: NF:mmcobj.ISnapinPropertiesCallback.AddPropertyName
title: ISnapinPropertiesCallback::AddPropertyName
author: windows-sdk-content
description: The AddPropertyName method adds a property, by name, for the snap-in to use.
old-location: mmc\isnapinpropertiescallback_addpropertyname.htm
tech.root: MMC
ms.assetid: 44f2536b-c224-4704-b99a-6e7ef21961bc
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: AddPropertyName, AddPropertyName method [MMC], AddPropertyName method [MMC],ISnapinPropertiesCallback interface, ISnapinPropertiesCallback interface [MMC],AddPropertyName method, ISnapinPropertiesCallback.AddPropertyName, ISnapinPropertiesCallback::AddPropertyName, MMC_PROP_CHANGEAFFECTSUI, MMC_PROP_MODIFIABLE, MMC_PROP_PERSIST, MMC_PROP_REMOVABLE, _slate_isnapinpropertiescallback_addpropertyname, mmc.isnapinpropertiescallback_addpropertyname, mmcobj/ISnapinPropertiesCallback::AddPropertyName
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mmcobj.h
req.include-header: 
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
req.lib: 
req.dll: Mmcndmgr.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmcndmgr.dll
api_name:
 - ISnapinPropertiesCallback.AddPropertyName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- mmcobj.h
: 
- ISnapinPropertiesCallback.AddPropertyName
: 
---

# ISnapinPropertiesCallback::AddPropertyName


## -description


The 
<b>AddPropertyName</b> method adds a property, by name, for the snap-in to use.


## -parameters




### -param pszPropName [in]

The property name.


### -param dwFlags [in]

This parameter can be one or more of the following flags.



#### MMC_PROP_CHANGEAFFECTSUI

If modified, the property affects the user interface.



#### MMC_PROP_MODIFIABLE

The property can be modified.



#### MMC_PROP_REMOVABLE

The property can be deleted.



#### MMC_PROP_PERSIST

The property can be saved.


## -returns



If successful, the return value is S_OK. Other return values indicate an error code.



