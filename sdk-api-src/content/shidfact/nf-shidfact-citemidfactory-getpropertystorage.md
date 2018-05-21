---
UID: NF:shidfact.CItemIDFactory.GetPropertyStorage
title: CItemIDFactory::GetPropertyStorage
author: windows-driver-content
description: Gets a read only pointer to the serialized property storage that is used for storing metadata.
old-location: shell\citemidfactory_getpropertystorage.htm
old-project: shell
ms.assetid: 3A3F0F28-C9E1-4F2E-9A02-C6A48BF3C204
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: CItemIDFactory interface [Windows Shell],GetPropertyStorage method, CItemIDFactory.GetPropertyStorage, CItemIDFactory::GetPropertyStorage, GetPropertyStorage, GetPropertyStorage method [Windows Shell], GetPropertyStorage method [Windows Shell],CItemIDFactory interface, shell.citemidfactory_getpropertystorage, shidfact/CItemIDFactory::GetPropertyStorage
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
req.typenames: SHELL_UI_COMPONENT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	shidfact.h
api_name:
-	CItemIDFactory.GetPropertyStorage
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5.0
---

# CItemIDFactory::GetPropertyStorage


## -description


Gets  a read only pointer to the serialized property storage that is used for storing metadata.


## -parameters




### -param pidl [in, optional]

A PIDL that contains the location of the property storage.


### -param pcb [out]

When this method returns, contains the size, in bytes, of the storage.


## -returns



If this method succeeds, it returns a read only pointer to the serialized property storage.




## -see-also




<a href="https://msdn.microsoft.com/8C13F1AF-3328-40B8-B5F8-6CDF753A7FA7">CItemIDFactory</a>
 

 

