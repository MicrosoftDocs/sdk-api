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

# SHBindToParent function


## -description


Takes a pointer to a fully qualified item identifier list (PIDL), and returns a specified interface pointer on the parent object.


## -parameters




### -param pidl [in]

Type: <b>PCIDLIST_ABSOLUTE</b>

The item's PIDL.


### -param riid [in]

Type: <b>REFIID</b>

The <b>REFIID</b> of one of the interfaces exposed by the item's parent object.


### -param ppv [out]

Type: <b>VOID**</b>

A pointer to the interface specified by <i>riid</i>. You must release the object when you are finished.


### -param ppidlLast [out]

Type: <b>PCUITEMID_CHILD*</b>

The item's PIDL relative to the parent folder. This PIDL can be used with many of the methods supported by the parent folder's interfaces. If you set <i>ppidlLast</i> to <b>NULL</b>, the PIDL is not returned.



<div class="alert"><b>Note</b>  <b>SHBindToParent</b> does not allocate a new PIDL; it simply receives a pointer through this parameter. Therefore, you are not responsible for freeing this resource.</div>
<div> </div>

## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



