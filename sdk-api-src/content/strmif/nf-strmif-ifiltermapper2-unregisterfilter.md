---
UID: NF:strmif.IFilterMapper2.UnregisterFilter
title: IFilterMapper2::UnregisterFilter (strmif.h)
author: windows-sdk-content
description: The UnregisterFilter method removes filter information from the registry.
old-location: dshow\ifiltermapper2_unregisterfilter.htm
tech.root: DirectShow
ms.assetid: cfba764d-ec94-49a2-9aaf-2b107b742f83
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFilterMapper2 interface [DirectShow],UnregisterFilter method, IFilterMapper2.UnregisterFilter, IFilterMapper2::UnregisterFilter, IFilterMapper2UnregisterFilter, UnregisterFilter, UnregisterFilter method [DirectShow], UnregisterFilter method [DirectShow],IFilterMapper2 interface, dshow.ifiltermapper2_unregisterfilter, strmif/IFilterMapper2::UnregisterFilter
ms.topic: method
f1_keywords: 
 - "strmif/IFilterMapper2.UnregisterFilter"
dev_langs:
 - c++
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFilterMapper2::UnregisterFilter


## -description



The <code>UnregisterFilter</code> method removes filter information from the registry.




## -parameters




### -param pclsidCategory [in]

Address of a GUID that specifies the filter category from which to remove the filter. For a list of categories, see <a href="https://docs.microsoft.com/windows/desktop/DirectShow/filter-categories">Filter Categories</a>.


### -param szInstance [in]

Instance data used to construct the device moniker's display name. Use the value that was originally passed to the <b>RegisterFilter</b> method.


### -param Filter [in]

Class identifier (CLSID) of the filter.


## -returns



Returns S_OK if successful, or an <b>HRESULT</b> value indicating the cause of the error.




## -remarks



If the filter was not registered, the method might return an error.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ifiltermapper2">IFilterMapper2 Interface</a>
 

 

