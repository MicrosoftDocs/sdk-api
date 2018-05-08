---
UID: NF:shidfact.CItemIDFactory.GetPropertyFromIDList
title: CItemIDFactory::GetPropertyFromIDList
author: windows-driver-content
description: Gets a property from the IPropertyStore within the IDList as a variant, using the key.
old-location: shell\citemidfactory_getpropertyfromidlist_key.htm
old-project: shell
ms.assetid: 2BC0557F-57B2-4389-ABC6-9186A4FCF814
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: CItemIDFactory interface [Windows Shell],GetPropertyFromIDList method, CItemIDFactory.GetPropertyFromIDList, CItemIDFactory::GetPropertyFromIDList, GetPropertyFromIDList, GetPropertyFromIDList method [Windows Shell], GetPropertyFromIDList method [Windows Shell],CItemIDFactory interface, shell.citemidfactory_getpropertyfromidlist_key, shidfact/CItemIDFactory::GetPropertyFromIDList
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
-	CItemIDFactory.GetPropertyFromIDList
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5.0
---

# CItemIDFactory::GetPropertyFromIDList


## -description


Gets a property from the <a href="https://msdn.microsoft.com/library/windows/hardware/ff536954">IPropertyStore</a> within the IDList as a variant, using the key.


## -parameters




### -param pidl [in]

A PIDL identifying the <a href="https://msdn.microsoft.com/library/windows/hardware/ff536954">IPropertyStore</a>.


#### - rkey [in]

The key for the selected property.


#### - pvar [out]

When this method returns, contains a pointer to the property. If <i>rkey</i> is not found, <i>pvar</i> will be <b>VT_EMPTY</b>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is useful when using <a href="https://msdn.microsoft.com/f006828c-980d-4e36-be68-3b3c238cd884">IShellFolder2::GetDetailsEx</a>, as is returns a variant rather than a <b>PROPVARIANT</b>.




## -see-also




<a href="https://msdn.microsoft.com/8C13F1AF-3328-40B8-B5F8-6CDF753A7FA7">CItemIDFactory</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff536954">IPropertyStore</a>



<a href="https://msdn.microsoft.com/f006828c-980d-4e36-be68-3b3c238cd884">IShellFolder2::GetDetailsEx</a>
 

 

