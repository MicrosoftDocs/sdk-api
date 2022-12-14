---
UID: NF:propsys.IPropertyDescriptionSearchInfo.GetProjectionString
title: IPropertyDescriptionSearchInfo::GetProjectionString (propsys.h)
description: Returns a pointer to a string containing the canonical name of the item.
helpviewer_keywords: ["GetProjectionString","GetProjectionString method [Windows Properties]","GetProjectionString method [Windows Properties]","IPropertyDescriptionSearchInfo interface","IPropertyDescriptionSearchInfo interface [Windows Properties]","GetProjectionString method","IPropertyDescriptionSearchInfo.GetProjectionString","IPropertyDescriptionSearchInfo::GetProjectionString","_shell_IPropertyDescriptionSearchInfo_GetProjectionString","properties.IPropertyDescriptionSearchInfo_GetProjectionString","propsys/IPropertyDescriptionSearchInfo::GetProjectionString","shell.IPropertyDescriptionSearchInfo_GetProjectionString"]
old-location: properties\IPropertyDescriptionSearchInfo_GetProjectionString.htm
tech.root: properties
ms.assetid: 06881c29-fafb-47be-abdb-906e289ee5fc
ms.date: 12/05/2018
ms.keywords: GetProjectionString, GetProjectionString method [Windows Properties], GetProjectionString method [Windows Properties],IPropertyDescriptionSearchInfo interface, IPropertyDescriptionSearchInfo interface [Windows Properties],GetProjectionString method, IPropertyDescriptionSearchInfo.GetProjectionString, IPropertyDescriptionSearchInfo::GetProjectionString, _shell_IPropertyDescriptionSearchInfo_GetProjectionString, properties.IPropertyDescriptionSearchInfo_GetProjectionString, propsys/IPropertyDescriptionSearchInfo::GetProjectionString, shell.IPropertyDescriptionSearchInfo_GetProjectionString
req.header: propsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Propsys.idl
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
 - IPropertyDescriptionSearchInfo::GetProjectionString
 - propsys/IPropertyDescriptionSearchInfo::GetProjectionString
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Propsys.h
api_name:
 - IPropertyDescriptionSearchInfo.GetProjectionString
---

# IPropertyDescriptionSearchInfo::GetProjectionString


## -description

Returns a pointer to a string containing the canonical name of the item.

## -parameters

### -param ppszProjection [out]

Type: <b>LPWSTR*</b>

When this method returns successfully, contains a pointer to a string containing the canonical name of the item.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

