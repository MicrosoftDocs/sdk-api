---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IEnumWiaItem::Clone


## -description


The <b>IEnumWiaItem::Clone</b> method creates an additional instance of the <a href="https://msdn.microsoft.com/25eab463-a531-4cb7-b8b7-6b1c8d060ee8">IEnumWiaItem</a> interface and sends back a pointer to it.


## -parameters




### -param ppIEnum [out]

Type: <b><a href="https://msdn.microsoft.com/25eab463-a531-4cb7-b8b7-6b1c8d060ee8">IEnumWiaItem</a>**</b>

Pointer  to the <a href="https://msdn.microsoft.com/25eab463-a531-4cb7-b8b7-6b1c8d060ee8">IEnumWiaItem</a> interface. Receives the address of the <b>IEnumWiaItem</b> interface instance that <b>IEnumWiaItem::Clone</b> creates.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Applications must call the <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IUnknown::Release</a> method on the interface pointers they receive through the <i>ppIEnum</i> parameter.



