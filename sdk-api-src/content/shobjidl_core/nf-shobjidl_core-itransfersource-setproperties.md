---
UID: NF:shobjidl_core.ITransferSource.SetProperties
title: ITransferSource::SetProperties (shobjidl_core.h)
description: Sets properties that should be applied to an item.
helpviewer_keywords: ["ITransferSource interface [Windows Shell]","SetProperties method","ITransferSource.SetProperties","ITransferSource::SetProperties","SetProperties","SetProperties method [Windows Shell]","SetProperties method [Windows Shell]","ITransferSource interface","_shell_ITransferSource_SetProperties","shell.ITransferSource_SetProperties","shobjidl_core/ITransferSource::SetProperties"]
old-location: shell\ITransferSource_SetProperties.htm
tech.root: shell
ms.assetid: c42497cc-5a19-41da-9356-1086796032a7
ms.date: 12/05/2018
ms.keywords: ITransferSource interface [Windows Shell],SetProperties method, ITransferSource.SetProperties, ITransferSource::SetProperties, SetProperties, SetProperties method [Windows Shell], SetProperties method [Windows Shell],ITransferSource interface, _shell_ITransferSource_SetProperties, shell.ITransferSource_SetProperties, shobjidl_core/ITransferSource::SetProperties
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
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
 - ITransferSource::SetProperties
 - shobjidl_core/ITransferSource::SetProperties
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - ITransferSource.SetProperties
---

# ITransferSource::SetProperties


## -description

Sets properties that should be applied to an item.

## -parameters

### -param pproparray [in]

Type: <b><a href="/windows/desktop/api/propsys/nn-propsys-ipropertychangearray">IPropertyChangeArray</a>*</b>

An array of properties and their changed values.

## -returns

Type: <b>HRESULT</b>

Any return value other than S_OK indicates a failure.