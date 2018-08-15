---
UID: NF:shidfact.CItemIDFactory.GetPropertyFromIDList(PCUIDLIST_RELATIVE,PCWSTR,PROPVARIANT)
title: CItemIDFactory::GetPropertyFromIDList(PCUIDLIST_RELATIVE,PCWSTR,PROPVARIANT)
author: windows-sdk-content
description: Gets a property from the IPropertyStore within the IDList as a variant, using the key.
old-location: shell\citemidfactory_getpropertyfromidlist_key.htm
old-project: shell
ms.assetid: 2BC0557F-57B2-4389-ABC6-9186A4FCF814
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CItemIDFactory interface [Windows Shell],GetPropertyFromIDList method, CItemIDFactory.GetPropertyFromIDList, CItemIDFactory.GetPropertyFromIDList(PCUIDLIST_RELATIVE,PCWSTR,PROPVARIANT), CItemIDFactory::GetPropertyFromIDList, CItemIDFactory::GetPropertyFromIDList(PCUIDLIST_RELATIVE,PCWSTR,PROPVARIANT), GetPropertyFromIDList, GetPropertyFromIDList method [Windows Shell], GetPropertyFromIDList method [Windows Shell],CItemIDFactory interface, shell.citemidfactory_getpropertyfromidlist_key, shidfact/CItemIDFactory::GetPropertyFromIDList
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shidfact.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: SHELL_UI_COMPONENT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shidfact.h
api_name:
 - GetPropertyFromIDList.GetPropertyFromIDList
 - CItemIDFactory.GetPropertyFromIDList
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5.0
---

# CItemIDFactory::GetPropertyFromIDList(PCUIDLIST_RELATIVE,PCWSTR,PROPVARIANT)


## -description


Gets a property from the <a href="https://msdn.microsoft.com/e995aaa1-d4c9-475f-b1fa-b9123cd5b653">IPropertyStore</a> within the IDList as a variant, using the key.


## -parameters




### -param pidl [in]

A PIDL identifying the <a href="https://msdn.microsoft.com/e995aaa1-d4c9-475f-b1fa-b9123cd5b653">IPropertyStore</a>.


### -param pszName




### -param pv






#### - pvar [out]

When this method returns, contains a pointer to the property. If <i>rkey</i> is not found, <i>pvar</i> will be <b>VT_EMPTY</b>.


#### - rkey [in]

The key for the selected property.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is useful when using <a href="https://msdn.microsoft.com/f006828c-980d-4e36-be68-3b3c238cd884">IShellFolder2::GetDetailsEx</a>, as is returns a variant rather than a <b>PROPVARIANT</b>.




## -see-also




<a href="https://msdn.microsoft.com/8C13F1AF-3328-40B8-B5F8-6CDF753A7FA7">CItemIDFactory</a>



<a href="https://msdn.microsoft.com/D0BE2A9A-5832-4C0E-BFB6-96EB467C3D9D">GetPropertyFromIDList</a>



<a href="https://msdn.microsoft.com/e995aaa1-d4c9-475f-b1fa-b9123cd5b653">IPropertyStore</a>



<a href="https://msdn.microsoft.com/f006828c-980d-4e36-be68-3b3c238cd884">IShellFolder2::GetDetailsEx</a>
 

 

