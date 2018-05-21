---
UID: NF:propsys.INamedPropertyStore.SetNamedValue
title: INamedPropertyStore::SetNamedValue
author: windows-driver-content
description: Sets the value of a named property.
old-location: shell\INamedPropertyStore_SetNamedValue.htm
old-project: shell
ms.assetid: e1ccf53f-3117-45c2-a0ff-94f1bb084414
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: INamedPropertyStore interface [Windows Shell],SetNamedValue method, INamedPropertyStore.SetNamedValue, INamedPropertyStore::SetNamedValue, SetNamedValue, SetNamedValue method [Windows Shell], SetNamedValue method [Windows Shell],INamedPropertyStore interface, _shell_INamedPropertyStore_SetNamedValue, propsys/INamedPropertyStore::SetNamedValue, shell.INamedPropertyStore_SetNamedValue
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
-	INamedPropertyStore.SetNamedValue
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# INamedPropertyStore::SetNamedValue


## -description


Sets the value of a named property.


## -parameters




### -param pszName [in]

Type: <b>LPCWSTR</b>

A pointer to the property name, as a Unicode string, in the named property store.


### -param propvar






#### - pv [in]

Type: <b>const <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>*</b>


          A pointer to a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure that contains the value to set for the property named in <i>pszName</i>.
        


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



