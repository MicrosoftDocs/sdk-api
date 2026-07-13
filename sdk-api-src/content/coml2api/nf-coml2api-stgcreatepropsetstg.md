---
UID: NF:coml2api.StgCreatePropSetStg
title: StgCreatePropSetStg function (coml2api.h)
description: Creates a property set storage object from a specified storage object.
helpviewer_keywords: ["StgCreatePropSetStg","StgCreatePropSetStg function [Structured Storage]","_stg_stgcreatepropsetstg","coml2api/StgCreatePropSetStg","stg.stgcreatepropsetstg"]
old-location: stg\stgcreatepropsetstg.htm
tech.root: Stg
ms.assetid: 0113b29d-23aa-4590-b8ac-33789a7a2ed4
ms.date: 12/05/2018
ms.keywords: StgCreatePropSetStg, StgCreatePropSetStg function [Structured Storage], _stg_stgcreatepropsetstg, coml2api/StgCreatePropSetStg, stg.stgcreatepropsetstg
req.header: coml2api.h
req.include-header: Propidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - StgCreatePropSetStg
 - coml2api/StgCreatePropSetStg
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-com-ole32-l1-1-5.dll
 - Ole32.dll
 - API-MS-Win-Core-Com-l2-1-1.dll
 - coml2.dll
api_name:
 - StgCreatePropSetStg
---

# StgCreatePropSetStg function


## -description

The <b>StgCreatePropSetStg</b> function creates a property set storage object from a specified storage object. The property set storage object supplies the system-provided, stand-alone implementation of the 
<a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage">IPropertySetStorage</a> interface.

## -parameters

### -param pStorage [in]

A pointer to the storage object that contains or will contain one or more property sets.

### -param dwReserved

Reserved for future use; must be zero.

### -param ppPropSetStg [out]

A pointer to 
<a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage">IPropertySetStorage</a>* pointer variable that receives the interface pointer to the property-set storage object.

## -returns

This function supports the standard return value <b>E_INVALIDARG</b> as well as the following:

## -remarks

The 
<b>StgCreatePropSetStg</b> function creates an 
<a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage">IPropertySetStorage</a> interface that will act on the given 
<a href="/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a> interface specified by the <i>pStorage</i> parameter. This function does not modify this 
<b>IStorage</b> by itself, although subsequent calls to the 
<b>IPropertySetStorage</b> interface might.

<b>StgCreatePropSetStg</b> calls <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">IUnknown::AddRef</a> on the storage object specified by <i>pStorage</i>. The caller must release the object when it is no longer required by calling <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a>.


#### Examples

The following example code shows how this function  creates a property set within a storage object.


```cpp
IPropertyStorage*
CreatePropertySetInStorage( IStorage *pStg, const FMTID &fmtid )
{
    HRESULT hr = S_OK;
    IPropertySetStorage *pPropSetStg = NULL;
    IPropertyStorage *pPropStg = NULL;
 
    try
    {
        hr = StgCreatePropSetStg( pStg, 0, &pPropSetStg );
        if( FAILED(hr) ) throw L"Failed StgCreatePropSetStg (%08x)";
 
        hr = pPropSetStg->Create( fmtid, NULL,
            PROPSETFLAG_DEFAULT,
            STGM_CREATE | STGM_READWRITE | STGM_SHARE_EXCLUSIVE,
            &pPropStg );
        if( FAILED(hr) ) 
            throw L"Failed IPropertySetStorage::Create (%08x)";
 
        // Success. The caller must now call Release on both
        // pPropSetStg and pStg.
 
    }
    catch( const WCHAR *pwszError )
    {
        wprintf( L"Error: %s (%08x)\n", pwszError, hr );
    }
 
    if( NULL != pPropSetStg )
        pPropSetStg->Release();
 
    return( pPropStg );
}
```

## -see-also

<a href="/windows/desktop/Stg/ipropertysetstorage-stand-alone-implementation">IPropertySetStorage-Stand-alone Implementation</a>



<a href="/windows/desktop/Stg/samples">Samples</a>



<a href="/windows/desktop/Stg/stgcreatepropsetstg-sample">StgCreatePropSetStg Sample</a>