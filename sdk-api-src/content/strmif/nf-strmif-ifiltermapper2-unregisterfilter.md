---
UID: NF:strmif.IFilterMapper2.UnregisterFilter
title: IFilterMapper2::UnregisterFilter
author: windows-sdk-content
description: The UnregisterFilter method removes filter information from the registry.
old-location: dshow\ifiltermapper2_unregisterfilter.htm
old-project: DirectShow
ms.assetid: cfba764d-ec94-49a2-9aaf-2b107b742f83
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: IFilterMapper2 interface [DirectShow],UnregisterFilter method, IFilterMapper2.UnregisterFilter, IFilterMapper2::UnregisterFilter, IFilterMapper2UnregisterFilter, UnregisterFilter, UnregisterFilter method [DirectShow], UnregisterFilter method [DirectShow],IFilterMapper2 interface, dshow.ifiltermapper2_unregisterfilter, strmif/IFilterMapper2::UnregisterFilter
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IFilterMapper2.UnregisterFilter
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IFilterMapper2::UnregisterFilter


## -description



The <code>UnregisterFilter</code> method removes filter information from the registry.




## -parameters




### -param pclsidCategory [in]

Address of a GUID that specifies the filter category from which to remove the filter. For a list of categories, see <a href="https://msdn.microsoft.com/cab4e2c9-eab9-4836-adfc-870490ca5b6b">Filter Categories</a>.


### -param szInstance [in]

Instance data used to construct the device moniker's display name. Use the value that was originally passed to the <b>RegisterFilter</b> method.


### -param Filter [in]

Class identifier (CLSID) of the filter.


## -returns



Returns S_OK if successful, or an <b>HRESULT</b> value indicating the cause of the error.




## -remarks



If the filter was not registered, the method might return an error.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/6a3db838-cee3-4a9f-a924-fb55931acc83">IFilterMapper2 Interface</a>
 

 

