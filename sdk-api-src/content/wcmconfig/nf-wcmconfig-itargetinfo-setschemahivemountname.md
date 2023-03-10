---
UID: NF:wcmconfig.ITargetInfo.SetSchemaHiveMountName
title: ITargetInfo::SetSchemaHiveMountName (wcmconfig.h)
description: Sets the name of the mount location of the schema hive.
helpviewer_keywords: ["ITargetInfo interface [SMI]","SetSchemaHiveMountName method","ITargetInfo.SetSchemaHiveMountName","ITargetInfo::SetSchemaHiveMountName","SetSchemaHiveMountName","SetSchemaHiveMountName method [SMI]","SetSchemaHiveMountName method [SMI]","ITargetInfo interface","smi.itargetinfo_setschemahivemountname","wcmconfig/ITargetInfo::SetSchemaHiveMountName"]
old-location: smi\itargetinfo_setschemahivemountname.htm
tech.root: SMI
ms.assetid: 128cf457-c66e-49b7-88a7-3f5d87800a20
ms.date: 12/05/2018
ms.keywords: ITargetInfo interface [SMI],SetSchemaHiveMountName method, ITargetInfo.SetSchemaHiveMountName, ITargetInfo::SetSchemaHiveMountName, SetSchemaHiveMountName, SetSchemaHiveMountName method [SMI], SetSchemaHiveMountName method [SMI],ITargetInfo interface, smi.itargetinfo_setschemahivemountname, wcmconfig/ITargetInfo::SetSchemaHiveMountName
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
 - ITargetInfo::SetSchemaHiveMountName
 - wcmconfig/ITargetInfo::SetSchemaHiveMountName
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
 - ITargetInfo.SetSchemaHiveMountName
---

# ITargetInfo::SetSchemaHiveMountName


## -description

Sets the name of the mount location of the schema hive.

## -parameters

### -param pwzMountName [in]

The mount location of the schema hive.

## -returns

This method returns an HRESULT value. <b>S_OK</b> indicates success. May return <b>E_OUTOFMEMORY</b> if the system is low on resources.

## -see-also

<a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-itargetinfo">ITargetInfo</a>