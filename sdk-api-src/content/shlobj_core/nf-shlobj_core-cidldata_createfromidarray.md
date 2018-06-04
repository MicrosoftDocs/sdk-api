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

# CIDLData_CreateFromIDArray function


## -description


<p class="CCE_Message">[<b>CIDLData_CreateFromIDArray</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Creates a data object with the default vtable pointer.


## -parameters




### -param pidlFolder [in]

Type: <b>PCIDLIST_ABSOLUTE</b>

A fully qualified IDLIST for the root of the items specified in <i>apidl</i>.


### -param cidl [in]

Type: <b>UINT</b>

The number of entries in the <i>apidl</i> array.


### -param apidl [in]

Type: <b>PCUIDLIST_RELATIVE_ARRAY</b>

The array of item IDs relative to <i>pidlFolder</i>. Typically, <i>apidl</i> is an array of child IDs and <i>pidlFolder</i> is a full PIDL for those items. However, <i>pidlFolder</i> can be a null PIDL (desktop IDLISTs). In that case, <i>apidl</i> can contain fully qualified ID lists.


### -param ppdtobj [out]

Type: <b><a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a>**</b>

The address to a pointer to the object that implements <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a>.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The data object created by this function offers the Shell clipboard format identifier <a href="https://msdn.microsoft.com/fb8ce5d3-3215-4e05-a916-4d4a803464d2">CFSTR_SHELLIDLIST</a>. This data object also supports <a href="https://msdn.microsoft.com/7430d12c-ab07-4a9c-a845-4743818afbc7">IDataObject::SetData</a> calls to pick up other clipboard formats.




## -see-also




<a href="https://msdn.microsoft.com/d56cdafe-9463-43a5-8ef0-6cfaf0c524a8">SHCreateDataObject</a>
 

 

