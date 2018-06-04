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

# SHMapPIDLToSystemImageListIndex function


## -description


<p class="CCE_Message">[<b>SHMapPIDLToSystemImageListIndex</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Retrieves the icon index from the system image list that is associated with a folder item.


## -parameters




### -param pshf

TBD


### -param pidl [in]

Type: <b>PCUITEMID_CHILD</b>

A pointer to the item's <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structure.


### -param piIndexSel

TBD




#### - piIndex [out, optional]

Type: <b>int*</b>

A pointer to an <b>int</b> that, when this function returns successfully, receives the index of the item's <b>open</b> icon in the system image list. If the item does not have a special <b>open</b> icon then the index of its normal icon is returned. If the <b>open</b> icon exists and cannot be obtained, then the value pointed to by <i>piIndex</i> is set to -1. This parameter can be <b>NULL</b> if the calling application is not interested in the <b>open</b> icon.


#### - psf [in]

Type: <b><a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a>*</b>

An <a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a> interface pointer for the folder that contains the item.


## -returns



Type: <b>int</b>

Returns the index of the item's normal icon in the system image list if successful, or -1 otherwise.



