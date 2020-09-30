---
UID: NF:iads.IDirectoryObject.SetObjectAttributes
title: IDirectoryObject::SetObjectAttributes (iads.h)
description: The IDirectoryObject::SetObjectAttributes method modifies data in one or more specified object attributes defined in the ADS_ATTR_INFO structure.
helpviewer_keywords: ["IDirectoryObject interface [ADSI]","SetObjectAttributes method","IDirectoryObject.SetObjectAttributes","IDirectoryObject::SetObjectAttributes","SetObjectAttributes","SetObjectAttributes method [ADSI]","SetObjectAttributes method [ADSI]","IDirectoryObject interface","_ds_idirectoryobject_setobjectattributes","adsi.idirectoryobject__setobjectattributes","adsi.idirectoryobject_setobjectattributes","iads/IDirectoryObject::SetObjectAttributes"]
old-location: adsi\idirectoryobject_setobjectattributes.htm
tech.root: adsi
ms.assetid: 999e6766-52cf-4087-bb17-72de487975c2
ms.date: 12/05/2018
ms.keywords: IDirectoryObject interface [ADSI],SetObjectAttributes method, IDirectoryObject.SetObjectAttributes, IDirectoryObject::SetObjectAttributes, SetObjectAttributes, SetObjectAttributes method [ADSI], SetObjectAttributes method [ADSI],IDirectoryObject interface, _ds_idirectoryobject_setobjectattributes, adsi.idirectoryobject__setobjectattributes, adsi.idirectoryobject_setobjectattributes, iads/IDirectoryObject::SetObjectAttributes
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
 - IDirectoryObject::SetObjectAttributes
 - iads/IDirectoryObject::SetObjectAttributes
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
 - IDirectoryObject.SetObjectAttributes
---

# IDirectoryObject::SetObjectAttributes


## -description

The <b>IDirectoryObject::SetObjectAttributes</b> method modifies data in one or more specified object attributes defined in the  <a href="/windows/desktop/api/iads/ns-iads-ads_attr_info">ADS_ATTR_INFO</a> structure.

## -parameters

### -param pAttributeEntries [in]

Provides an array of attributes to be modified. Each attribute contains the name of the attribute, the operation to perform, and the attribute value, if applicable. For more information, see the  <a href="/windows/desktop/api/iads/ns-iads-ads_attr_info">ADS_ATTR_INFO</a> structure.

### -param dwNumAttributes [in]

Provides the number of attributes to be modified. This value should correspond to the size of the <i>pAttributeEntries</i> array.

### -param pdwNumAttributesModified [out]

Provides a pointer to a <b>DWORD</b> variable that contains the number of attributes modified by the <b>SetObjectAttributes</b> method.

## -returns

This method returns the standard return values, including S_OK when the attributes are set successfully.

For more information and other return values, see  <a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>.

## -remarks

In Active Directory (LDAP provider), the <b>IDirectoryObject::SetObjectAttributes</b> method is a transacted call. The attributes are either all committed or discarded. Other directory providers may not transact the call.

Active Directory does not allow duplicate values on a multi-valued attribute. However, if you call <b>SetObjectAttributes</b> to append a duplicate value to a multi-valued attribute of an Active Directory object, the <b>SetObjectAttributes</b> call succeeds but the duplicate value is ignored.

Similarly, if you use <b>SetObjectAttributes</b> to delete one or more values from a multi-valued property of an Active Directory object, the operation succeeds even if any or all of the specified values are not set for the property


#### Examples

The following C++ code example sets the <b>sn</b> attribute of a user object to the value of <b>Price</b> as a case-insensitive string.


```cpp
HRESULT hr;
IDirectoryObject *pDirObject=NULL;
DWORD  dwReturn;
ADSVALUE  snValue;
ADS_ATTR_INFO attrInfo[] = { {L"sn",ADS_ATTR_UPDATE, ADSTYPE_CASE_IGNORE_STRING, &snValue, 1} };
DWORD dwAttrs = sizeof(attrInfo)/sizeof(ADS_ATTR_INFO); 
 
snValue.dwType=ADSTYPE_CASE_IGNORE_STRING;
snValue.CaseIgnoreString = L"Price";
 
hr = ADsGetObject(L"LDAP://CN=Jeff Smith,OU=Sales,DC=Fabrikam,DC=com",
        IID_IDirectoryObject, 
        (void**) &pDirObject );
 
if ( SUCCEEDED(hr) )
{
    hr = pDirObject->SetObjectAttributes(attrInfo, dwAttrs, &dwReturn);

    pDirObject->Release();
}

```

## -see-also

<a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>



<a href="/windows/desktop/api/iads/ns-iads-ads_attr_info">ADS_ATTR_INFO</a>



<a href="/windows/desktop/api/iads/nn-iads-idirectoryobject">IDirectoryObject</a>