---
UID: NF:shidfact.CItemIDFactory.GetPropertyStorageFromIDList
title: CItemIDFactory::GetPropertyStorageFromIDList
author: windows-sdk-content
description: Create an instance of the IPropertyStore based on the serialized property storage associated with the first ItemID.
old-location: shell\citemidfactory_getpropertystoragefromidlist.htm
tech.root: shell
ms.assetid: 50E8F4F9-1E7B-4314-9AFB-1CA0795776FE
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: CItemIDFactory interface [Windows Shell],GetPropertyStorageFromIDList method, CItemIDFactory.GetPropertyStorageFromIDList, CItemIDFactory::GetPropertyStorageFromIDList, GetPropertyStorageFromIDList, GetPropertyStorageFromIDList method [Windows Shell], GetPropertyStorageFromIDList method [Windows Shell],CItemIDFactory interface, shell.citemidfactory_getpropertystoragefromidlist, shidfact/CItemIDFactory::GetPropertyStorageFromIDList
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shidfact.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - shidfact.h
api_name:
 - CItemIDFactory.GetPropertyStorageFromIDList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CItemIDFactory::GetPropertyStorageFromIDList


## -description


create an instance of the <a href="https://msdn.microsoft.com/e995aaa1-d4c9-475f-b1fa-b9123cd5b653">IPropertyStore</a> based on the serialized property storage associated with the first ItemID.


## -parameters




### -param pidl [in]

A PIDL containing the serialized property storage.


### -param riid [in]

A reference to the IID of the <a href="https://msdn.microsoft.com/e995aaa1-d4c9-475f-b1fa-b9123cd5b653">IPropertyStore</a> that is obtained by using __uuidof(IPropertyStore).


### -param ppv [out]

When this method returns, contains the address of a pointer to a new <a href="https://msdn.microsoft.com/e995aaa1-d4c9-475f-b1fa-b9123cd5b653">IPropertyStore</a>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/8C13F1AF-3328-40B8-B5F8-6CDF753A7FA7">CItemIDFactory</a>



<a href="https://msdn.microsoft.com/e995aaa1-d4c9-475f-b1fa-b9123cd5b653">IPropertyStore</a>
 

 

