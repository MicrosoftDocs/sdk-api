---
UID: NF:iads.IADsPropertyList.Skip
title: IADsPropertyList::Skip (iads.h)
description: Skips a specified number of items, counting from the current cursor position, in the property list.
helpviewer_keywords: ["IADsPropertyList interface [ADSI]","Skip method","IADsPropertyList.Skip","IADsPropertyList::Skip","Skip","Skip method [ADSI]","Skip method [ADSI]","IADsPropertyList interface","_ds_iadspropertylist_skip","adsi.iadspropertylist__skip","adsi.iadspropertylist_skip","iads/IADsPropertyList::Skip"]
old-location: adsi\iadspropertylist_skip.htm
tech.root: adsi
ms.assetid: 3bbdf1e8-444c-4d5e-83df-95a1f4fd7508
ms.date: 12/05/2018
ms.keywords: IADsPropertyList interface [ADSI],Skip method, IADsPropertyList.Skip, IADsPropertyList::Skip, Skip, Skip method [ADSI], Skip method [ADSI],IADsPropertyList interface, _ds_iadspropertylist_skip, adsi.iadspropertylist__skip, adsi.iadspropertylist_skip, iads/IADsPropertyList::Skip
req.header: iads.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.dll: Activeds.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IADsPropertyList::Skip
 - iads/IADsPropertyList::Skip
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Activeds.dll
api_name:
 - IADsPropertyList.Skip
---

# IADsPropertyList::Skip


## -description

The <b>IADsPropertyList::Skip</b> method skips a specified number of items, counting from the current cursor position, in the property list.

## -parameters

### -param cElements [in]

Number of elements to be skipped.

## -returns

This method supports the standard HRESULT return values, including S_OK. For more information and other return values, see  <a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>.

## -see-also

<a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>



<a href="/windows/desktop/api/iads/nn-iads-iadspropertylist">IADsPropertyList</a>



<a href="/windows/desktop/ADSI/iadspropertylist-property-methods">IADsPropertyList Property Methods</a>



<a href="/windows/desktop/api/iads/nf-iads-iadspropertylist-next">IADsPropertyList::Next</a>