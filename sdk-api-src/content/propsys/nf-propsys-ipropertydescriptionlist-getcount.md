---
UID: NF:propsys.IPropertyDescriptionList.GetCount
title: IPropertyDescriptionList::GetCount
author: windows-driver-content
description: Gets the number of properties included in the property list.
old-location: properties\IPropertyDescriptionList_GetCount.htm
old-project: properties
ms.assetid: 17d8b018-1709-42a7-9edf-e1c2886593de
ms.author: windowsdriverdev
ms.date: 4/27/2018
ms.keywords: GetCount, GetCount method [Windows Properties], GetCount method [Windows Properties],IPropertyDescriptionList interface, IPropertyDescriptionList interface [Windows Properties],GetCount method, IPropertyDescriptionList.GetCount, IPropertyDescriptionList::GetCount, _shell_IPropertyDescriptionList_GetCount, properties.IPropertyDescriptionList_GetCount, propsys/IPropertyDescriptionList::GetCount, shell.IPropertyDescriptionList_GetCount
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: propsys.h
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
req.typenames: PSC_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	propsys.h
api_name:
-	IPropertyDescriptionList.GetCount
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IPropertyDescriptionList::GetCount


## -description


Gets the number of properties included in the property list.


## -parameters




### -param pcElem [out]

Type: <b>UINT*</b>

When this method returns, contains a pointer to the count of properties.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



