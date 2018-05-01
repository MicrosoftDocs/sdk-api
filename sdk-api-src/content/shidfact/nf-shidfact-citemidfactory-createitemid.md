---
UID: NF:shidfact.CItemIDFactory.CreateItemID
title: CItemIDFactory::CreateItemID method
author: windows-driver-content
description: Creates an ItemID from the supplied data.
old-location: shell\citemidfactory_createitemid.htm
old-project: shell
ms.assetid: 2129F4F3-A989-4CE2-ABFF-FE83DD78D4CE
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: CItemIDFactory, CItemIDFactory interface [Windows Shell], CreateItemID method, CItemIDFactory::CreateItemID, CreateItemID method [Windows Shell], CreateItemID method [Windows Shell], CItemIDFactory interface, CreateItemID,CItemIDFactory.CreateItemID, shell.citemidfactory_createitemid, shidfact/CItemIDFactory::CreateItemID
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
-	CItemIDFactory.CreateItemID
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5.0
---

# CItemIDFactory::CreateItemID method


## -description


Creates an ItemID from the supplied data.


## -parameters




### -param pinner [in, optional]

A pointer to the client structure that should be copied.


### -param pps [in, out, optional]

A pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff536954">IPropertyStore</a> that will be seriallized into the ItemID.


### -param ppidl [out]

When this method returns, contains a pointer to the ItemID containing the client data and <a href="https://msdn.microsoft.com/library/windows/hardware/ff536954">IPropertyStore</a> data.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The size of the user supplied data must equal sizeof(T). Do not use structs with variably allocated array/string members. The struct must also follow standard <a href="https://msdn.microsoft.com/794c8425-2319-4339-881c-c5083ab05638">SHITEMID</a> for persistance and portability.




## -see-also




<a href="https://msdn.microsoft.com/8C13F1AF-3328-40B8-B5F8-6CDF753A7FA7">CItemIDFactory</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff536954">IPropertyStore</a>



<a href="https://msdn.microsoft.com/794c8425-2319-4339-881c-c5083ab05638">SHITEMID</a>
 

 

