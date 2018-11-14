---
UID: NF:propsys.IPropertyDescriptionSearchInfo.GetMaxSize
title: IPropertyDescriptionSearchInfo::GetMaxSize
author: windows-sdk-content
description: Gets the maximum size value from the property schema's searchInfo element.
old-location: properties\IPropertyDescriptionSearchInfo_GetMaxSize.htm
tech.root: properties
ms.assetid: a1d5812a-0166-4d63-93a7-c6dc2a6e247d
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: GetMaxSize, GetMaxSize method [Windows Properties], GetMaxSize method [Windows Properties],IPropertyDescriptionSearchInfo interface, IPropertyDescriptionSearchInfo interface [Windows Properties],GetMaxSize method, IPropertyDescriptionSearchInfo.GetMaxSize, IPropertyDescriptionSearchInfo::GetMaxSize, _shell_IPropertyDescriptionSearchInfo_GetMaxSize, properties.IPropertyDescriptionSearchInfo_GetMaxSize, propsys/IPropertyDescriptionSearchInfo::GetMaxSize, shell.IPropertyDescriptionSearchInfo_GetMaxSize
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Propsys.h
api_name:
 - IPropertyDescriptionSearchInfo.GetMaxSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- propsys.h
: 
- IPropertyDescriptionSearchInfo.GetMaxSize
: 
---

# IPropertyDescriptionSearchInfo::GetMaxSize


## -description


Gets the maximum size value from the property schema's <a href="shell.propdesc_schema_searchInfo">searchInfo</a> element.


## -parameters




### -param pcbMaxSize [out]

Type: <b>UINT*</b>

Pointer to a value that, when this method returns successfully, receives the value of the maxSize attribute of the <a href="shell.propdesc_schema_searchInfo">searchInfo</a> element. The default is:

                    

<ul>
<li><b>Windows Vista</b>: 128 bytes</li>
<li><b>Windows 7 and later</b>: 512 bytes</li>
</ul>

## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



