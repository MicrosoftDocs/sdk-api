---
UID: NF:mmcobj.ISnapinProperties.QueryPropertyNames
title: ISnapinProperties::QueryPropertyNames (mmcobj.h)
description: The QueryPropertyNames method returns the names of the properties used for the snap-in's configuration.
helpviewer_keywords: ["ISnapinProperties interface [MMC]","QueryPropertyNames method","ISnapinProperties.QueryPropertyNames","ISnapinProperties::QueryPropertyNames","QueryPropertyNames","QueryPropertyNames method [MMC]","QueryPropertyNames method [MMC]","ISnapinProperties interface","_slate_isnapinproperties_querypropertynames","mmc.isnapinproperties_querypropertynames","mmcobj/ISnapinProperties::QueryPropertyNames"]
old-location: mmc\isnapinproperties_querypropertynames.htm
tech.root: mmc
ms.assetid: 41f949aa-4be5-4e60-aa1d-0605f489fec6
ms.date: 12/05/2018
ms.keywords: ISnapinProperties interface [MMC],QueryPropertyNames method, ISnapinProperties.QueryPropertyNames, ISnapinProperties::QueryPropertyNames, QueryPropertyNames, QueryPropertyNames method [MMC], QueryPropertyNames method [MMC],ISnapinProperties interface, _slate_isnapinproperties_querypropertynames, mmc.isnapinproperties_querypropertynames, mmcobj/ISnapinProperties::QueryPropertyNames
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISnapinProperties::QueryPropertyNames
 - mmcobj/ISnapinProperties::QueryPropertyNames
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmcobj.h
api_name:
 - ISnapinProperties.QueryPropertyNames
---

# ISnapinProperties::QueryPropertyNames


## -description

The 
<b>QueryPropertyNames</b> method returns the names of the properties used for the snap-in's configuration.

## -parameters

### -param pCallback [in]

A pointer to the 
<a href="/windows/desktop/api/mmcobj/nn-mmcobj-isnapinpropertiescallback">ISnapinPropertiesCallback</a> interface; the snap-in can call 
<a href="/windows/desktop/api/mmcobj/nf-mmcobj-isnapinpropertiescallback-addpropertyname">ISnapinPropertiesCallback::AddPropertyName</a> to add the properties.

## -returns

If successful, the return value is S_OK; otherwise, the return value is an error code.