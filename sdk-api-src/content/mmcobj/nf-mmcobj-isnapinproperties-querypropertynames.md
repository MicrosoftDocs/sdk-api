---
UID: NF:mmcobj.ISnapinProperties.QueryPropertyNames
title: ISnapinProperties::QueryPropertyNames
author: windows-sdk-content
description: The QueryPropertyNames method returns the names of the properties used for the snap-in's configuration.
old-location: mmc\isnapinproperties_querypropertynames.htm
old-project: MMC
ms.assetid: 41f949aa-4be5-4e60-aa1d-0605f489fec6
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: ISnapinProperties interface [MMC],QueryPropertyNames method, ISnapinProperties.QueryPropertyNames, ISnapinProperties::QueryPropertyNames, QueryPropertyNames, QueryPropertyNames method [MMC], QueryPropertyNames method [MMC],ISnapinProperties interface, _slate_isnapinproperties_querypropertynames, mmc.isnapinproperties_querypropertynames, mmcobj/ISnapinProperties::QueryPropertyNames
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mmcobj.h
req.include-header: 
req.redist: 
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
req.typenames: MMC_PROPERTY_ACTION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmcobj.h
api_name:
 - ISnapinProperties.QueryPropertyNames
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# ISnapinProperties::QueryPropertyNames


## -description


The 
<b>QueryPropertyNames</b> method returns the names of the properties used for the snap-in's configuration.


## -parameters




### -param pCallback [in]

A pointer to the 
<a href="https://msdn.microsoft.com/d02d265c-f3fa-4332-910e-f0d9d4f0687a">ISnapinPropertiesCallback</a> interface; the snap-in can call 
<a href="https://msdn.microsoft.com/44f2536b-c224-4704-b99a-6e7ef21961bc">ISnapinPropertiesCallback::AddPropertyName</a> to add the properties.


## -returns



If successful, the return value is S_OK; otherwise, the return value is an error code.



