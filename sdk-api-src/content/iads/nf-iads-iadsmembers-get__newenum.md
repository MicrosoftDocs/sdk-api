---
UID: NF:iads.IADsMembers.get__NewEnum
title: IADsMembers::get__NewEnum (iads.h)
description: The IADsMembers::get__NewEnum method gets a dependent enumerator object that implements IEnumVARIANT for this ADSI collection object. Be aware that there are two underscore characters in the function name (get__NewEnum).
helpviewer_keywords: ["IADsMembers interface [ADSI]","get__NewEnum method","IADsMembers.get__NewEnum","IADsMembers::get__NewEnum","_ds_iadsmembers_get__newenum","adsi.iadsmembers__get____newenum","adsi.iadsmembers_get__newenum","get__NewEnum","get__NewEnum method [ADSI]","get__NewEnum method [ADSI]","IADsMembers interface","iads/IADsMembers::get__NewEnum"]
old-location: adsi\iadsmembers_get__newenum.htm
tech.root: adsi
ms.assetid: 5a65794c-2407-4267-bc02-d84a134f6bf4
ms.date: 12/05/2018
ms.keywords: IADsMembers interface [ADSI],get__NewEnum method, IADsMembers.get__NewEnum, IADsMembers::get__NewEnum, _ds_iadsmembers_get__newenum, adsi.iadsmembers__get____newenum, adsi.iadsmembers_get__newenum, get__NewEnum, get__NewEnum method [ADSI], get__NewEnum method [ADSI],IADsMembers interface, iads/IADsMembers::get__NewEnum
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
 - IADsMembers::get__NewEnum
 - iads/IADsMembers::get__NewEnum
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
 - IADsMembers.get__NewEnum
---

# IADsMembers::get__NewEnum


## -description

The <b>IADsMembers::get__NewEnum</b> method gets a dependent enumerator object that implements  <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant">IEnumVARIANT</a> for this ADSI collection object. Be aware that there are two underscore characters in the function name (<b>get__NewEnum</b>).

## -parameters

### -param ppEnumerator [out]

Pointer to a pointer to the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface on the enumerator object for this collection.

## -returns

This method supports the standard return values, including S_OK. For more information about other return values, see  <a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>.

## -see-also

<a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>



<a href="/windows/desktop/api/iads/nn-iads-iadsmembers">IADsMembers</a>



<a href="/windows/desktop/ADSI/iadsmembers-property-methods">IADsMembers Property Methods</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant">IEnumVARIANT</a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>