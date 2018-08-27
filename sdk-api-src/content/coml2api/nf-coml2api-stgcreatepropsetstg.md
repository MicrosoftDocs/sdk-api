---
UID: NF:coml2api.StgCreatePropSetStg
title: StgCreatePropSetStg function
author: windows-sdk-content
description: Creates a property set storage object from a specified storage object.
old-location: stg\stgcreatepropsetstg.htm
old-project: stg
ms.assetid: 0113b29d-23aa-4590-b8ac-33789a7a2ed4
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: StgCreatePropSetStg, StgCreatePropSetStg function [Structured Storage], _stg_stgcreatepropsetstg, coml2api/StgCreatePropSetStg, stg.stgcreatepropsetstg
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: coml2api.h
req.include-header: Propidl.h
req.redist: 
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
tech.root: 
req.typenames: CATEGORYINFO, *LPCATEGORYINFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
 - API-MS-Win-Core-Com-l2-1-1.dll
 - coml2.dll
api_name:
 - StgCreatePropSetStg
product: Windows
targetos: Windows
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
---

# StgCreatePropSetStg function


## -description


The <b>StgCreatePropSetStg</b> function creates a property set storage object from a specified storage object. The property set storage object supplies the system-provided, stand-alone implementation of the 
<a href="https://msdn.microsoft.com/en-us/library/Aa379840(v=VS.85).aspx">IPropertySetStorage</a> interface.


## -parameters




### -param pStorage [in]

A pointer to the storage object that contains or will contain one or more property sets.


### -param dwReserved

Reserved for future use; must be zero.


### -param ppPropSetStg [out]

A pointer to 
<a href="https://msdn.microsoft.com/en-us/library/Aa379840(v=VS.85).aspx">IPropertySetStorage</a>* pointer variable that receives the interface pointer to the property-set storage object.


## -returns



This function supports the standard return value <b>E_INVALIDARG</b> as well as the following:




## -remarks



The 
<b>StgCreatePropSetStg</b> function creates an 
<a href="https://msdn.microsoft.com/en-us/library/Aa379840(v=VS.85).aspx">IPropertySetStorage</a> interface that will act on the given 
<a href="https://msdn.microsoft.com/en-us/library/Aa380015(v=VS.85).aspx">IStorage</a> interface specified by the <i>pStorage</i> parameter. This function does not modify this 
<b>IStorage</b> by itself, although subsequent calls to the 
<b>IPropertySetStorage</b> interface might.

<b>StgCreatePropSetStg</b> calls <a href="https://msdn.microsoft.com/en-us/library/ms691379(v=VS.85).aspx">IUnknown::AddRef</a> on the storage object specified by <i>pStorage</i>. The caller must release the object when it is no longer required by calling <a href="https://msdn.microsoft.com/en-us/library/ms682317(v=VS.85).aspx">Release</a>.


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




<a href="https://msdn.microsoft.com/en-us/library/Aa379966(v=VS.85).aspx">IPropertySetStorage-Stand-alone Implementation</a>



<a href="https://msdn.microsoft.com/0c48da47-b718-48fe-8ad0-39686bb83283">Samples</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa380326(v=VS.85).aspx">StgCreatePropSetStg Sample</a>
 

 

