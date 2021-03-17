---
UID: NF:iads.IADsExtension.PrivateGetIDsOfNames
title: IADsExtension::PrivateGetIDsOfNames (iads.h)
description: The IADsExtension::PrivateGetIDsOfNames method is called by the aggregator, ADSI, after ADSI determines that the extension is used to support a dual or dispatch interface. The method can use the type data to get DISPID using IDispatch::GetIDsOfNames.
helpviewer_keywords: ["IADsExtension interface [ADSI]","PrivateGetIDsOfNames method","IADsExtension.PrivateGetIDsOfNames","IADsExtension::PrivateGetIDsOfNames","PrivateGetIDsOfNames","PrivateGetIDsOfNames method [ADSI]","PrivateGetIDsOfNames method [ADSI]","IADsExtension interface","_ds_iadsextension_privategetidsofnames","adsi.iadsextension__privategetidsofnames","adsi.iadsextension_privategetidsofnames","iads/IADsExtension::PrivateGetIDsOfNames"]
old-location: adsi\iadsextension_privategetidsofnames.htm
tech.root: adsi
ms.assetid: 533faef7-d504-443c-83e7-7eaf461ce550
ms.date: 12/05/2018
ms.keywords: IADsExtension interface [ADSI],PrivateGetIDsOfNames method, IADsExtension.PrivateGetIDsOfNames, IADsExtension::PrivateGetIDsOfNames, PrivateGetIDsOfNames, PrivateGetIDsOfNames method [ADSI], PrivateGetIDsOfNames method [ADSI],IADsExtension interface, _ds_iadsextension_privategetidsofnames, adsi.iadsextension__privategetidsofnames, adsi.iadsextension_privategetidsofnames, iads/IADsExtension::PrivateGetIDsOfNames
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
 - IADsExtension::PrivateGetIDsOfNames
 - iads/IADsExtension::PrivateGetIDsOfNames
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
 - IADsExtension.PrivateGetIDsOfNames
---

# IADsExtension::PrivateGetIDsOfNames


## -description

The <b>IADsExtension::PrivateGetIDsOfNames</b> method is called by the aggregator, ADSI, after ADSI determines that the extension is used to support a dual or dispatch interface. The method can use the type data to get DISPID using  <a href="/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-getidsofnames">IDispatch::GetIDsOfNames</a>.

## -parameters

### -param riid

Reserved for future use. It must be IID_NULL.

### -param rgszNames

Passed-in array of names to be mapped.

### -param cNames

Count of the names to be mapped.

### -param lcid

The locale context in which to interpret the names.

### -param rgDispid

Caller-allocated array, each element of which contains an identifier that corresponds to one of the names passed in the <i>rgszNames</i> array. The first element represents the member name. The subsequent elements represent each of the member's parameters.

## -returns

The return values are the same as those of the standard <a href="/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-getidsofnames">IDispatch::GetIDsOfNames</a> method. For more information about other return values, see  <a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>.

## -remarks

All the parameters have the same meaning as the corresponding ones in the standard <a href="/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-getidsofnames">IDispatch::GetIDsOfNames</a>(). The extension component returns a unique identifier (<i>rgDispID</i>) for each method or property defined in the supported dual interfaces. The uniqueness is enforced within the extension component. The ADSI provider must ensure the uniqueness of the DISPIDs of all extension objects and the aggregator (ADSI) itself. The <i>rgDispID</i> parameter must be between 1 and 16777215 (2^24-1), or -1 (DISPID_UNKNOWN).


#### Examples

The following C/C++ code example shows a generic implementation of this method.


```cpp
STDMETHOD(PrivateGetIDsOfNames)(REFIID riid, OLECHAR ** rgszNames, unsigned int cNames, LCID lcid, DISPID  * rgdispid)
{
  if (rgdispid == NULL)
  {
     return E_POINTER;
  }
  return  DispGetIDsOfNames(m_pTypeInfo, rgszNames, cNames, rgdispid);
}
```

## -see-also

<a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>



<a href="/windows/desktop/api/iads/nn-iads-iadsextension">IADsExtension</a>



<a href="/windows/desktop/api/iads/nf-iads-iadsextension-privateinvoke">IADsExtension::PrivateInvoke</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-getidsofnames">IDispatch::GetIDsOfNames</a>