---
UID: NE:filter.tagIFILTER_FLAGS
title: tagIFILTER_FLAGS
author: windows-driver-content
description: Indicates whether the caller should use the IPropertySetStorage and IPropertyStorage interfaces to locate additional properties.
old-location: indexsrv\ifilter_flags.htm
old-project: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixrefint_0j03.htm
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IFILTER_FLAGS, IFILTER_FLAGS enumeration [Indexing Service], IFILTER_FLAGS_OLE_PROPERTIES, _idxs_IFILTER_FLAGS, filter/IFILTER_FLAGS, filter/IFILTER_FLAGS_OLE_PROPERTIES, indexsrv.ifilter_flags, tagIFILTER_FLAGS
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: IFILTER_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Filter.h
api_name:
-	IFILTER_FLAGS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5
---

# tagIFILTER_FLAGS enumeration


## -description


<p class="CCE_Message">[Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use <a href="https://msdn.microsoft.com/6da601c6-3742-40ad-99f2-8817f7f642b3">Windows Search</a> for client side search and  <a href=" http://go.microsoft.com/fwlink/p/?linkid=258445">Microsoft Search Server Express</a> for server side search.]

Indicates whether the caller should use the <b>IPropertySetStorage</b> and <b>IPropertyStorage</b> interfaces to locate additional properties.


## -enum-fields




### -field IFILTER_FLAGS_OLE_PROPERTIES

The caller should use the <a href="_stg_ipropertysetstorage">IPropertySetStorage</a> and <a href="_stg_ipropertystorage">IPropertyStorage</a> interfaces to locate additional properties. When this flag is set, properties available through COM enumerators should not be returned from <a href="https://msdn.microsoft.com/5fb7219a-608c-43f8-a8e3-48bbf0218c6e">IFilter</a>.


## -remarks



The <i>pdwFlags</i> parameter in the <a href="https://msdn.microsoft.com/5cb9b675-258e-46b0-905f-15a086f84f74">IFilter::Init</a> method allows the <a href="https://msdn.microsoft.com/5fb7219a-608c-43f8-a8e3-48bbf0218c6e">IFilter</a> implementation to pass information back to the caller. For Indexing Service 3.0, the only valid flag is IFILTER_FLAGS_OLE_PROPERTIES. If OLE properties should not be enumerated, then pdwFlags should be set to zero.




## -see-also




<a href="https://msdn.microsoft.com/5fb7219a-608c-43f8-a8e3-48bbf0218c6e">IFilter</a>



<a href="_stg_ipropertysetstorage">IPropertySetStorage</a>



<a href="_stg_ipropertystorage">IPropertyStorage</a>
 

 

