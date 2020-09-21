---
UID: NS:subsmgr._tagITEMPROP
title: ITEMPROP (subsmgr.h)
description: Stores information about properties in the Windows Property System, and is used by the IItemPropertyBag interface.
helpviewer_keywords: ["*LPITEMPROP","ITEMPROP","ITEMPROP structure [search]","PITEMPROP","PITEMPROP structure pointer [search]","search.itemprop","subsmgr/ITEMPROP","subsmgr/PITEMPROP"]
old-location: search\itemprop.htm
tech.root: search
ms.assetid: 480C84CB-60CE-42F4-ADE6-4FCF1EAF15AF
ms.date: 12/05/2018
ms.keywords: '*LPITEMPROP, ITEMPROP, ITEMPROP structure [search], PITEMPROP, PITEMPROP structure pointer [search], search.itemprop, subsmgr/ITEMPROP, subsmgr/PITEMPROP'
req.header: subsmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
targetos: Windows
req.typenames: ITEMPROP, *LPITEMPROP
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
f1_keywords:
 - _tagITEMPROP
 - subsmgr/_tagITEMPROP
 - LPITEMPROP
 - subsmgr/LPITEMPROP
 - ITEMPROP
 - subsmgr/ITEMPROP
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - subsmgr.h
api_name:
 - ITEMPROP
---

# ITEMPROP structure


## -description

<p class="CCE_Message">[<b>ITEMPROP</b> and <a href="/windows/desktop/search/iitempropertybag">IItemPropertyBag</a> are supported only on Windows XP and Windows Server 2003, and should no longer be used.]

Stores information about properties in the <a href="/windows/desktop/properties/windows-properties-system">Windows Property System</a>, and is used by the <a href="/windows/desktop/search/iitempropertybag">IItemPropertyBag</a> interface.

## -struct-fields

### -field variantValue

### -field pwszName

 




#### - bstrIndexProp

The name of a property in the <a href="/windows/desktop/properties/windows-properties-system">Windows Property System</a>. For example, the <a href="/windows/desktop/properties/props-system-itemurl">System.ItemUrl</a> property.


#### - bstrName

For internal use only.


#### - ds

For internal use only.


#### - dwHint

For internal use only.


#### - dwUID

For internal use only.


#### - vt

The type of the property value. For example, the type of the string property <a href="/windows/desktop/properties/props-system-itemurl">System.ItemUrl</a> is <b>VT_BSTR</b>.

## -remarks

To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the <a href="/windows/desktop/search/iitempropertybag">IItemPropertyBag</a> interface and the following APIs: the <a href="/windows/desktop/search/-search-isearchprotocolui">ISearchProtocolUI</a>, <a href="/windows/desktop/search/-search-iitempreviewerext">IItemPreviewerExt</a> and <a href="/windows/desktop/search/-search-isearchitem">ISearchItem</a> interfaces, the <a href="/windows/desktop/search/-search-linkinfo">LINKINFO</a> and <b>ITEMPROP</b> structures, and the <a href="/windows/desktop/search/-search-linktype">LINKTYPE</a> enumeration.

## -see-also

<a href="/windows/desktop/search/iitempropertybag">IItemPropertyBag</a>