---
UID: NF:iads.IDirectoryObject.CreateDSObject
title: IDirectoryObject::CreateDSObject (iads.h)
description: Creates a child of the current directory service object.
helpviewer_keywords: ["CreateDSObject","CreateDSObject method [ADSI]","CreateDSObject method [ADSI]","IDirectoryObject interface","IDirectoryObject interface [ADSI]","CreateDSObject method","IDirectoryObject.CreateDSObject","IDirectoryObject::CreateDSObject","_ds_idirectoryobject_createdsobject","adsi.idirectoryobject__createdsobject","adsi.idirectoryobject_createdsobject","iads/IDirectoryObject::CreateDSObject"]
old-location: adsi\idirectoryobject_createdsobject.htm
tech.root: adsi
ms.assetid: 77648d1c-b05b-4c36-a2e3-25bb5713d615
ms.date: 12/05/2018
ms.keywords: CreateDSObject, CreateDSObject method [ADSI], CreateDSObject method [ADSI],IDirectoryObject interface, IDirectoryObject interface [ADSI],CreateDSObject method, IDirectoryObject.CreateDSObject, IDirectoryObject::CreateDSObject, _ds_idirectoryobject_createdsobject, adsi.idirectoryobject__createdsobject, adsi.idirectoryobject_createdsobject, iads/IDirectoryObject::CreateDSObject
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
 - IDirectoryObject::CreateDSObject
 - iads/IDirectoryObject::CreateDSObject
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
 - IDirectoryObject.CreateDSObject
---

# IDirectoryObject::CreateDSObject


## -description

The <b>IDirectoryObject::CreateDSObject</b> method creates a child of the current directory service object.

## -parameters

### -param pszRDNName [in]

Provides the relative distinguished name (relative path) of the object to be created.

### -param pAttributeEntries [in]

An array of  <a href="/windows/desktop/api/iads/ns-iads-ads_attr_info">ADS_ATTR_INFO</a> structures that contain attribute definitions to be set when the object is created.

### -param dwNumAttributes [in]

Provides a number of attributes set when the object is created.

### -param ppObject [out]

Provides a pointer to the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface on the created object.

## -returns

This method returns the standard return values, including S_OK for a successful operation. For more information and other return values, see  <a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>.

## -remarks

Specify all attributes to be initialized on creation in the <i>pAttributeEntries</i> array. You may also specify optional attributes. When creating a directory object with this method, attributes with any of the string data types cannot be empty or zero-length.


#### Examples

The following C/C++ code example shows how to create a user object using the <b>IDirectoryObject::CreateDSObject</b> method.


```cpp
HRESULT    hr;
IDirectoryObject *pDirObject=NULL;
ADSVALUE   sAMValue;
ADSVALUE   uPNValue;
ADSVALUE   classValue;
LPDISPATCH pDisp;
 
ADS_ATTR_INFO  attrInfo[] = 
{  
   { L"objectClass", ADS_ATTR_UPDATE, 
                       ADSTYPE_CASE_IGNORE_STRING, &classValue, 1 },
   {L"sAMAccountName", ADS_ATTR_UPDATE, 
                       ADSTYPE_CASE_IGNORE_STRING, &sAMValue, 1},
   {L"userPrincipalName", ADS_ATTR_UPDATE, 
                      ADSTYPE_CASE_IGNORE_STRING, &uPNValue, 1},
};
DWORD dwAttrs = sizeof(attrInfo)/sizeof(ADS_ATTR_INFO); 
 
classValue.dwType = ADSTYPE_CASE_IGNORE_STRING;
classValue.CaseIgnoreString = L"user";
 
sAMValue.dwType=ADSTYPE_CASE_IGNORE_STRING;
sAMValue.CaseIgnoreString = L"jeffsmith";
 
uPNValue.dwType=ADSTYPE_CASE_IGNORE_STRING;
uPNValue.CaseIgnoreString = L"jeffsmith@Fabrikam.com";
 
hr = ADsGetObject(L"LDAP://OU=Sales,DC=Fabrikam,DC=com",
          IID_IDirectoryObject, (void**) &pDirObject );
 
if ( SUCCEEDED(hr) )
{
    hr = pDirObject->CreateDSObject( L"CN=Jeff Smith",  attrInfo, 
                                    dwAttrs, &pDisp );

    if ( SUCCEEDED(hr) )
    {
         // Use the DS object.

         pDisp->Release();
    }

    pDirObject->Release();
}

```

## -see-also

<a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>



<a href="/windows/desktop/api/iads/ns-iads-ads_attr_info">ADS_ATTR_INFO</a>



<a href="/windows/desktop/api/iads/nn-iads-idirectoryobject">IDirectoryObject</a>