---
UID: NE:filter.tagIFILTER_FLAGS
title: tagIFILTER_FLAGS
author: windows-sdk-content
description: Indicates whether the caller should use the IPropertySetStorage and IPropertyStorage interfaces to locate additional properties.
old-location: search\_search_IFILTER_FLAGS.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\enums\ifilter_flags.htm
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IFILTER_FLAGS, IFILTER_FLAGS enumeration [search], IFILTER_FLAGS_OLE_PROPERTIES, _search_IFILTER_FLAGS, filter/IFILTER_FLAGS, filter/IFILTER_FLAGS_OLE_PROPERTIES, search._search_IFILTER_FLAGS, tagIFILTER_FLAGS
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: filter.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Filter.h
api_name:
 - IFILTER_FLAGS
product: Windows
targetos: Windows
req.typenames: IFILTER_FLAGS
req.redist: the Windows NT 4.0 Option Pack
---

# tagIFILTER_FLAGS enumeration


## -description


Indicates whether the caller should use the <a href="https://msdn.microsoft.com/en-us/library/Aa379840(v=VS.85).aspx">IPropertySetStorage</a> and <a href="https://msdn.microsoft.com/en-us/library/Aa379968(v=VS.85).aspx">IPropertyStorage</a> interfaces to locate additional properties.


## -enum-fields




### -field IFILTER_FLAGS_OLE_PROPERTIES

The caller should use the <a href="https://msdn.microsoft.com/en-us/library/Aa379840(v=VS.85).aspx">IPropertySetStorage</a> and <a href="https://msdn.microsoft.com/en-us/library/Aa379968(v=VS.85).aspx">IPropertyStorage</a> interfaces to locate additional properties. When this flag is set, properties available through COM enumerators should not be returned from <a href="https://msdn.microsoft.com/80b86ea0-d9d1-4d1f-b80f-90851e5bdf11">IFilter</a>. 


## -remarks



The <i>pdwFlags</i> parameter in the <a href="https://msdn.microsoft.com/c0ec3db9-23c4-449e-8106-572c432ea7cc">IFilter::Init</a> method allows the <a href="https://msdn.microsoft.com/80b86ea0-d9d1-4d1f-b80f-90851e5bdf11">IFilter</a> implementation to pass information back to the caller. For Windows Search, the only valid flag is IFILTER_FLAGS_OLE_PROPERTIES. If OLE properties should not be enumerated, then <i>pdwFlags</i> should be set to zero.




## -see-also




<a href="https://msdn.microsoft.com/80b86ea0-d9d1-4d1f-b80f-90851e5bdf11">IFilter</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa379840(v=VS.85).aspx">IPropertySetStorage</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa379968(v=VS.85).aspx">IPropertyStorage</a>



<a href="https://msdn.microsoft.com/c0ec3db9-23c4-449e-8106-572c432ea7cc">Init</a>



<b>Other Resources</b>



<b>Reference</b>
 

 

