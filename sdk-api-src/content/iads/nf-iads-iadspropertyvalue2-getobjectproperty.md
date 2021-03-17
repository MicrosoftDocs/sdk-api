---
UID: NF:iads.IADsPropertyValue2.GetObjectProperty
title: IADsPropertyValue2::GetObjectProperty (iads.h)
description: Retrieves an attribute value.
helpviewer_keywords: ["GetObjectProperty","GetObjectProperty method [ADSI]","GetObjectProperty method [ADSI]","IADsPropertyValue2 interface","IADsPropertyValue2 interface [ADSI]","GetObjectProperty method","IADsPropertyValue2.GetObjectProperty","IADsPropertyValue2::GetObjectProperty","_ds_iadspropertyvalue2_getobjectproperty","adsi.iadspropertyvalue2__getobjectproperty","adsi.iadspropertyvalue2_getobjectproperty","iads/IADsPropertyValue2::GetObjectProperty"]
old-location: adsi\iadspropertyvalue2_getobjectproperty.htm
tech.root: adsi
ms.assetid: a189f106-23dc-441b-8d97-c03d4c49a4a1
ms.date: 12/05/2018
ms.keywords: GetObjectProperty, GetObjectProperty method [ADSI], GetObjectProperty method [ADSI],IADsPropertyValue2 interface, IADsPropertyValue2 interface [ADSI],GetObjectProperty method, IADsPropertyValue2.GetObjectProperty, IADsPropertyValue2::GetObjectProperty, _ds_iadspropertyvalue2_getobjectproperty, adsi.iadspropertyvalue2__getobjectproperty, adsi.iadspropertyvalue2_getobjectproperty, iads/IADsPropertyValue2::GetObjectProperty
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
 - IADsPropertyValue2::GetObjectProperty
 - iads/IADsPropertyValue2::GetObjectProperty
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
 - IADsPropertyValue2.GetObjectProperty
---

# IADsPropertyValue2::GetObjectProperty


## -description

The <b>IADsPropertyValue2::GetObjectProperty</b> method retrieves an attribute value.

## -parameters

### -param lnADsType [in, out]

Pointer to a variable that, on entry, contains one of the <a href="/windows/win32/api/iads/ne-iads-adstypeenum">ADSTYPEENUM</a> values that specifies the data format that the value should be returned.

If the data type is not known, set this to <b>ADSTYPE_UNKNOWN</b>. In this case, this method will obtain the attribute value in the default data type and set this variable to the corresponding <a href="/windows/win32/api/iads/ne-iads-adstypeenum">ADSTYPEENUM</a> value. If any other <b>ADSTYPEENUM</b> value is specified, ADSI will return the attribute value only if the data type matches the format of the value.

### -param pvProp [out]

Pointer to a <b>VARIANT</b> that receives the requested attribute value. The variant type of this data will depend on the value returned in <i>lnADsType</i>. For more information and  a list of the <i>lnADsType</i> values and corresponding <i>pvProp</i> variant types, see <a href="/windows/desktop/api/iads/nn-iads-iadspropertyvalue2">IADsPropertyValue2</a>.

## -returns

Returns <b>S_OK</b> if successful or one of the following error codes.

## -see-also

<a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>



<a href="/windows/win32/api/iads/ne-iads-adstypeenum">ADSTYPEENUM</a>



<a href="/windows/desktop/api/iads/nn-iads-iadspropertyvalue">IADsPropertyValue</a>



<a href="/windows/desktop/api/iads/nn-iads-iadspropertyvalue2">IADsPropertyValue2</a>