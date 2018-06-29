---
UID: NF:propsys.INamedPropertyStore.GetNameCount
title: INamedPropertyStore::GetNameCount
author: windows-sdk-content
description: Gets the number of property names in the property store.
old-location: shell\INamedPropertyStore_GetNameCount.htm
old-project: shell
ms.assetid: 74bba1bf-e003-40bb-9118-4d647f78e409
ms.author: windowssdkdev
ms.date: 06/11/2018
ms.keywords: GetNameCount, GetNameCount method [Windows Shell], GetNameCount method [Windows Shell],INamedPropertyStore interface, INamedPropertyStore interface [Windows Shell],GetNameCount method, INamedPropertyStore.GetNameCount, INamedPropertyStore::GetNameCount, _shell_INamedPropertyStore_GetNameCount, propsys/INamedPropertyStore::GetNameCount, shell.INamedPropertyStore_GetNameCount
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
 - INamedPropertyStore.GetNameCount
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# INamedPropertyStore::GetNameCount


## -description


Gets the number of property names in the property store.


## -parameters




### -param pdwCount [out]

Type: <b>DWORD*</b>

When this method returns, contains a pointer to the count of names.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



