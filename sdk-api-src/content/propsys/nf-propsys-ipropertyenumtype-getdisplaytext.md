---
UID: NF:propsys.IPropertyEnumType.GetDisplayText
title: IPropertyEnumType::GetDisplayText method
author: windows-driver-content
description: Gets display text from an enumeration information structure.
old-location: properties\IPropertyEnumType_GetDisplayText.htm
old-project: properties
ms.assetid: d5168ca2-107f-45c2-80fa-21a2379776ed
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: GetDisplayText method [Windows Properties], GetDisplayText method [Windows Properties], IPropertyEnumType interface, GetDisplayText,IPropertyEnumType.GetDisplayText, IPropertyEnumType, IPropertyEnumType interface [Windows Properties], GetDisplayText method, IPropertyEnumType::GetDisplayText, _shell_IPropertyEnumType_GetDisplayText, properties.IPropertyEnumType_GetDisplayText, propsys/IPropertyEnumType::GetDisplayText, shell.IPropertyEnumType_GetDisplayText
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
req.typenames: PSC_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Propsys.h
api_name:
-	IPropertyEnumType.GetDisplayText
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IPropertyEnumType::GetDisplayText method


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



For additional information, see <a href="shell.propdesc_schema_enumeratedList">enumeratedList</a>.



