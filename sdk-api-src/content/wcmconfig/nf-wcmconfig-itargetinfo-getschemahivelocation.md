---
UID: NF:wcmconfig.ITargetInfo.GetSchemaHiveLocation
title: ITargetInfo::GetSchemaHiveLocation (wcmconfig.h)
description: Get the location of the schema hive.
helpviewer_keywords: ["GetSchemaHiveLocation","GetSchemaHiveLocation method [SMI]","GetSchemaHiveLocation method [SMI]","ITargetInfo interface","ITargetInfo interface [SMI]","GetSchemaHiveLocation method","ITargetInfo.GetSchemaHiveLocation","ITargetInfo::GetSchemaHiveLocation","smi.itargetinfo_getschemahivelocation","wcmconfig/ITargetInfo::GetSchemaHiveLocation"]
old-location: smi\itargetinfo_getschemahivelocation.htm
tech.root: SMI
ms.assetid: ad9accbd-0d23-40e6-8132-5a0c63a1b12a
ms.date: 12/05/2018
ms.keywords: GetSchemaHiveLocation, GetSchemaHiveLocation method [SMI], GetSchemaHiveLocation method [SMI],ITargetInfo interface, ITargetInfo interface [SMI],GetSchemaHiveLocation method, ITargetInfo.GetSchemaHiveLocation, ITargetInfo::GetSchemaHiveLocation, smi.itargetinfo_getschemahivelocation, wcmconfig/ITargetInfo::GetSchemaHiveLocation
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
req.lib: 
req.dll: SMIEngine.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITargetInfo::GetSchemaHiveLocation
 - wcmconfig/ITargetInfo::GetSchemaHiveLocation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SMIEngine.dll
api_name:
 - ITargetInfo.GetSchemaHiveLocation
---

# ITargetInfo::GetSchemaHiveLocation


## -description

Get the location of the schema hive.

## -parameters

### -param pHiveLocation [out]

A pointer to the schema hive location.

## -returns

This method returns an HRESULT value. <b>S_OK</b> indicates success. It returns <b>S_FALSE</b> if the location is not set. It may return <b>E_OUTOFMEMORY</b> if there are insufficient resources to return information to the user.

## -see-also

<a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-itargetinfo">ITargetInfo</a>