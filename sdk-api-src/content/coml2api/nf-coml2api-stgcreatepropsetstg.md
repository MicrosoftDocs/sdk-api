---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# StgCreatePropSetStg function


## -description



			The <b>StgCreatePropSetStg</b> function creates a property set storage object from a specified storage object. The property set storage object supplies the system-provided, stand-alone implementation of the 
<a href="https://msdn.microsoft.com/0ea3e1e0-c135-4138-81e4-f72412fc3128">IPropertySetStorage</a> interface.


## -parameters




### -param pStorage [in]

A pointer to the storage object that contains or will contain one or more property sets.


### -param dwReserved

Reserved for future use; must be zero.


### -param ppPropSetStg [out]

A pointer to 
<a href="https://msdn.microsoft.com/0ea3e1e0-c135-4138-81e4-f72412fc3128">IPropertySetStorage</a>* pointer variable that receives the interface pointer to the property-set storage object.


## -returns



This function supports the standard return value <b>E_INVALIDARG</b> as well as the following:




## -remarks



The 
<b>StgCreatePropSetStg</b> function creates an 
<a href="https://msdn.microsoft.com/0ea3e1e0-c135-4138-81e4-f72412fc3128">IPropertySetStorage</a> interface that will act on the given 
<a href="https://msdn.microsoft.com/2f454538-0f40-4811-b908-cd317ef79487">IStorage</a> interface specified by the <i>pStorage</i> parameter. This function does not modify this 
<b>IStorage</b> by itself, although subsequent calls to the 
<b>IPropertySetStorage</b> interface might.

<b>StgCreatePropSetStg</b> calls <a href="_com_iunknown_addref">IUnknown::AddRef</a> on the storage object specified by <i>pStorage</i>. The caller must release the object when it is no longer required by calling <a href="_com_iunknown_release">Release</a>.


#### Examples

The following example code shows how this function  creates a property set within a storage object.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>IPropertyStorage*
CreatePropertySetInStorage( IStorage *pStg, const FMTID &amp;fmtid )
{
    HRESULT hr = S_OK;
    IPropertySetStorage *pPropSetStg = NULL;
    IPropertyStorage *pPropStg = NULL;
 
    try
    {
        hr = StgCreatePropSetStg( pStg, 0, &amp;pPropSetStg );
        if( FAILED(hr) ) throw L"Failed StgCreatePropSetStg (%08x)";
 
        hr = pPropSetStg-&gt;Create( fmtid, NULL,
            PROPSETFLAG_DEFAULT,
            STGM_CREATE | STGM_READWRITE | STGM_SHARE_EXCLUSIVE,
            &amp;pPropStg );
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
        pPropSetStg-&gt;Release();
 
    return( pPropStg );
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/0ea5aadf-0b3f-44ac-9bb7-a7e8292f04c2">IPropertySetStorage-Stand-alone Implementation</a>



<a href="https://msdn.microsoft.com/0c48da47-b718-48fe-8ad0-39686bb83283">Samples</a>



<a href="https://msdn.microsoft.com/f0d0664a-2cfd-4eb0-b1d5-47d1545394fd">StgCreatePropSetStg Sample</a>
 

 

