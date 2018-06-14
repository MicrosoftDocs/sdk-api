---
UID: NF:propsys.IPropertyEnumType.GetDisplayText
title: IPropertyEnumType::GetDisplayText
author: windows-sdk-content
description: Gets display text from an enumeration information structure.
old-location: properties\IPropertyEnumType_GetDisplayText.htm
old-project: properties
ms.assetid: d5168ca2-107f-45c2-80fa-21a2379776ed
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: GetDisplayText, GetDisplayText method [Windows Properties], GetDisplayText method [Windows Properties],IPropertyEnumType interface, IPropertyEnumType interface [Windows Properties],GetDisplayText method, IPropertyEnumType.GetDisplayText, IPropertyEnumType::GetDisplayText, _shell_IPropertyEnumType_GetDisplayText, properties.IPropertyEnumType_GetDisplayText, propsys/IPropertyEnumType::GetDisplayText, shell.IPropertyEnumType_GetDisplayText
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: PSC_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Propsys.h
api_name:
 - IPropertyEnumType.GetDisplayText
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IPropertyEnumType::GetDisplayText


## -description


Gets display text from an enumeration information structure.


## -parameters




### -param ppszDisplay [out]

Type: <b>LPWSTR*</b>

When this method returns, contains the address of a pointer to a null-terminated Unicode string that contains the display text.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



For additional information, see <a href="https://www.bing.com/search?q=enumeratedList">enumeratedList</a>.



