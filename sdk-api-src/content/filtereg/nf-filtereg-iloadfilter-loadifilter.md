---
UID: NF:filtereg.ILoadFilter.LoadIFilter
title: ILoadFilter::LoadIFilter
author: windows-sdk-content
description: Retrieves and loads the most appropriate filter that is mapped to a Shell data source.
old-location: search\iloadfilter_loadifilter.htm
old-project: search
ms.assetid: 920c976e-4dde-4e53-85b7-7547291736a0
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: ILoadFilter interface [search],LoadIFilter method, ILoadFilter.LoadIFilter, ILoadFilter::LoadIFilter, LoadIFilter, LoadIFilter method [search], LoadIFilter method [search],ILoadFilter interface, filtereg/ILoadFilter::LoadIFilter, search.iloadfilter_loadifilter
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: filtereg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Filtereg.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: STAT_CHUNK
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - filtereg.h
api_name:
 - ILoadFilter.LoadIFilter
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5
---

# ILoadFilter::LoadIFilter


## -description


Retrieves and loads the most appropriate filter that is mapped to a Shell data source.



## -parameters




### -param pwcsPath [in]

Pointer to a comma-delimited null-terminated Unicode string buffer that specifies the path of the file to be filtered. This parameter can be null.


### -param pFilteredSources [in]

Pointer to the <a href="https://msdn.microsoft.com/5baae290-aead-4986-a7d4-0302931e0104">FILTERED_DATA_SOURCES</a> structure that specifies parameters for a Shell data source for which a filter is loaded. This parameter cannot be null.


### -param pUnkOuter [in]

If the object is being created as part of an aggregate, specify a pointer to the controlling <a href="http://msdn.microsoft.com/en-us/library/dd757099(VS.85).aspx">IUnknown</a> interface of the aggregate.


### -param fUseDefault [in]

If <b>TRUE</b>, use the default filter; if <b>FALSE</b>, proceed with the most appropriate filter that is available.


### -param pFilterClsid [in, out]

Pointer to the CLSID (CLSID_FilterRegistration) that receives the class identifier of the returned filter.


### -param SearchDecSize [in, out]

Not implemented.


### -param pwcsSearchDesc [in, out]

Not implemented.


### -param ppIFilt [in, out]

The address of a pointer to an implementation of an <a href="https://msdn.microsoft.com/library/ms691105(v=VS.85).aspx">IFilter</a> interface that <b>LoadIFilter</b> selects. 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



A filter, also known as a filter handler, is an implementation of the <a href="https://msdn.microsoft.com/library/ms691105(v=VS.85).aspx">IFilter</a> interface.

<b>ILoadFilter</b> attempts to load a filter that can process a Shell data source of the type specified in the <i>pFilteredSources</i> parameter through the <i>pwcsPath</i> parameter.

If an appropriate filter for the data source is not found, and <i>fUseDefault</i> is <b>false</b>, this method returns null in the <i>ppIFilt</i> parameter. If an appropriate filter for the data source is not found, and <i>fUseDefault</i> is <b>true</b>, the <a href="https://msdn.microsoft.com/library/ms691105(v=VS.85).aspx">IFilter</a> interface on the default <b>IFilter</b> is returned in the <i>ppIFilt</i> parameter.




## -see-also




<a href="https://msdn.microsoft.com/7ac51909-fa0e-4f97-8da0-0ab4c5de7d60">ILoadFilter</a>
 

 

