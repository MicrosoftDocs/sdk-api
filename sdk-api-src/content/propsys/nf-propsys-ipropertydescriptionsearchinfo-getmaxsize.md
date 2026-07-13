---
UID: NF:propsys.IPropertyDescriptionSearchInfo.GetMaxSize
title: IPropertyDescriptionSearchInfo::GetMaxSize (propsys.h)
description: Gets the maximum size value from the property schema's searchInfo element.
helpviewer_keywords: ["GetMaxSize","GetMaxSize method [Windows Properties]","GetMaxSize method [Windows Properties]","IPropertyDescriptionSearchInfo interface","IPropertyDescriptionSearchInfo interface [Windows Properties]","GetMaxSize method","IPropertyDescriptionSearchInfo.GetMaxSize","IPropertyDescriptionSearchInfo::GetMaxSize","_shell_IPropertyDescriptionSearchInfo_GetMaxSize","properties.IPropertyDescriptionSearchInfo_GetMaxSize","propsys/IPropertyDescriptionSearchInfo::GetMaxSize","shell.IPropertyDescriptionSearchInfo_GetMaxSize"]
old-location: properties\IPropertyDescriptionSearchInfo_GetMaxSize.htm
tech.root: properties
ms.assetid: a1d5812a-0166-4d63-93a7-c6dc2a6e247d
ms.date: 12/05/2018
ms.keywords: GetMaxSize, GetMaxSize method [Windows Properties], GetMaxSize method [Windows Properties],IPropertyDescriptionSearchInfo interface, IPropertyDescriptionSearchInfo interface [Windows Properties],GetMaxSize method, IPropertyDescriptionSearchInfo.GetMaxSize, IPropertyDescriptionSearchInfo::GetMaxSize, _shell_IPropertyDescriptionSearchInfo_GetMaxSize, properties.IPropertyDescriptionSearchInfo_GetMaxSize, propsys/IPropertyDescriptionSearchInfo::GetMaxSize, shell.IPropertyDescriptionSearchInfo_GetMaxSize
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
 - IPropertyDescriptionSearchInfo::GetMaxSize
 - propsys/IPropertyDescriptionSearchInfo::GetMaxSize
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
 - IPropertyDescriptionSearchInfo.GetMaxSize
---

# IPropertyDescriptionSearchInfo::GetMaxSize


## -description

Gets the maximum size value from the property schema's <a href="/windows/desktop/properties/propdesc-schema-searchinfo">searchInfo</a> element.

## -parameters

### -param pcbMaxSize [out]

Type: <b>UINT*</b>

Pointer to a value that, when this method returns successfully, receives the value of the maxSize attribute of the <a href="/windows/desktop/properties/propdesc-schema-searchinfo">searchInfo</a> element. The default is:

                    

<ul>
<li><b>Windows Vista</b>: 128 bytes</li>
<li><b>Windows 7 and later</b>: 512 bytes</li>
</ul>

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.