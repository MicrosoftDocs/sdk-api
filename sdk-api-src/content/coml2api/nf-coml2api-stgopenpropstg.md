---
UID: NF:coml2api.StgOpenPropStg
title: StgOpenPropStg function (coml2api.h)
description: Opens a specified property set in a specified storage or stream object.
helpviewer_keywords: ["StgOpenPropStg","StgOpenPropStg function [Structured Storage]","_stg_stgopenpropstg","coml2api/StgOpenPropStg","stg.stgopenpropstg"]
old-location: stg\stgopenpropstg.htm
tech.root: Stg
ms.assetid: ecc78e49-f1c2-4c2d-8390-b2b6f1dc776e
ms.date: 12/05/2018
ms.keywords: StgOpenPropStg, StgOpenPropStg function [Structured Storage], _stg_stgopenpropstg, coml2api/StgOpenPropStg, stg.stgopenpropstg
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
 - StgOpenPropStg
 - coml2api/StgOpenPropStg
dev_langs:
 - c++
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
 - StgOpenPropStg
---

# StgOpenPropStg function


## -description

The <b>StgOpenPropStg</b> function opens a specified property set in a specified storage or stream object. The property set supplies the system-provided, stand-alone implementation of the 
<a href="/windows/desktop/api/propidl/nn-propidl-ipropertystorage">IPropertyStorage</a> interface.

## -parameters

### -param pUnk [in]

The interface pointer for <b>IUnknown</b> interface on the storage or stream object that contains the requested property set object.

### -param fmtid [in]

The FMTID of the property set to be opened.

### -param grfFlags [in]

The values from <a href="/windows/desktop/Stg/propsetflag-constants">PROPSETFLAG Constants</a>.

### -param dwReserved [in]

Reserved for future use; must be zero.

### -param ppPropStg [out]

A pointer to 
an <a href="/windows/desktop/api/propidl/nn-propidl-ipropertystorage">IPropertyStorage</a>* pointer variable that receives the interface pointer to the requested property set.

## -returns

This function supports the standard return values E_INVALIDARG and E_UNEXPECTED, in addition to the following:

## -remarks

<b>StgOpenPropStg</b> opens the requested property set and supplies the system-provided, stand-alone implementation of the 
<a href="/windows/desktop/api/propidl/nn-propidl-ipropertystorage">IPropertyStorage</a> interface. The requested property set is contained in the storage or stream object specified by <i>pUnk</i>. The value of the <i>grfFlags</i> parameter indicates whether <i>pUnk</i> specifies a storage or stream object. For example, if PROPSETFLAG_NONSIMPLE is set, then <i>pUnk</i> can be queried for an 
<a href="/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a> interface on a storage object.

In either case, this function calls <i>pUnk-&gt;AddRef</i> for the storage or stream object containing the property set. The caller must release the object when no longer required.

This function is similar to the <a href="/windows/desktop/api/propidl/nf-propidl-ipropertysetstorage-open">IPropertySetStorage::Open</a> method. However, 
<b>StgOpenPropStg</b> adds the <i>pUnk</i> and <i>grfFlags</i> parameters, including the PROPSETFLAG_UNBUFFERED value for the <i>grfFlags</i> parameter. Use this function instead of the 
Open method if you have an 
<a href="/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a> interface that does not support the 
<a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage">IPropertySetStorage</a> interface, or if you want to use the PROPSETFLAG_UNBUFFERED value. For more information about using PROPSETFLAG_UNBUFFERED, see <a href="/windows/desktop/Stg/propsetflag-constants">PROPSETFLAG Constants</a>.

The <i>grfFlags</i> parameter is a combination of values taken from <a href="/windows/desktop/Stg/propsetflag-constants">PROPSETFLAG Constants</a>. The new enumeration value PROPSETFLAG_UNBUFFERED is supported. For more information, see 
<b>PROPSETFLAG Constants</b>.

This function is exported out of the redistributable iprop.dll, which is included in Windows NT 4.0 with Service Pack 2 (SP2) and available as a redistributable in Windows 95 and later. In Windows 2000, it is exported out of Ole32.dll. It can also be exported out of iprop.dll in Windows 2000, but the call gets forwarded to ole32.dll.

## -see-also

<a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage">IPropertySetStorage</a>



<a href="/windows/desktop/Stg/ipropertysetstorage-stand-alone-implementation">IPropertySetStorage-Stand-alone Implementation</a>



<a href="/windows/desktop/api/propidl/nn-propidl-ipropertystorage">IPropertyStorage</a>



<a href="/windows/desktop/Stg/ipropertystorage-stand-alone-implementation">IPropertyStorage-Stand-alone Implementation</a>



<a href="/windows/desktop/Stg/propsetflag-constants">PROPSETFLAG Constants</a>



<a href="/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropsetstg">StgCreatePropSetStg</a>



<a href="/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg">StgCreatePropStg</a>