---
UID: NF:iads.IDirectoryObject.GetObjectInformation
title: IDirectoryObject::GetObjectInformation (iads.h)
description: The IDirectoryObject::GetObjectInformation method retrieves a pointer to an ADS_OBJECT_INFO structure that contains data regarding the identity and location of a directory service object.
helpviewer_keywords: ["GetObjectInformation","GetObjectInformation method [ADSI]","GetObjectInformation method [ADSI]","IDirectoryObject interface","IDirectoryObject interface [ADSI]","GetObjectInformation method","IDirectoryObject.GetObjectInformation","IDirectoryObject::GetObjectInformation","_ds_idirectoryobject_getobjectinformation","adsi.idirectoryobject__getobjectinformation","adsi.idirectoryobject_getobjectinformation","iads/IDirectoryObject::GetObjectInformation"]
old-location: adsi\idirectoryobject_getobjectinformation.htm
tech.root: adsi
ms.assetid: 5a2d7fee-666e-4b3b-b6fa-b9f6d785c2c1
ms.date: 12/05/2018
ms.keywords: GetObjectInformation, GetObjectInformation method [ADSI], GetObjectInformation method [ADSI],IDirectoryObject interface, IDirectoryObject interface [ADSI],GetObjectInformation method, IDirectoryObject.GetObjectInformation, IDirectoryObject::GetObjectInformation, _ds_idirectoryobject_getobjectinformation, adsi.idirectoryobject__getobjectinformation, adsi.idirectoryobject_getobjectinformation, iads/IDirectoryObject::GetObjectInformation
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
 - IDirectoryObject::GetObjectInformation
 - iads/IDirectoryObject::GetObjectInformation
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
 - IDirectoryObject.GetObjectInformation
---

# IDirectoryObject::GetObjectInformation


## -description

The <b>IDirectoryObject::GetObjectInformation</b> method retrieves a pointer to an <a href="/windows/desktop/api/iads/ns-iads-ads_object_info">ADS_OBJECT_INFO</a> structure that contains data regarding the identity and location of a directory service object.

## -parameters

### -param ppObjInfo [out]

Provides the address of a pointer to an  <a href="/windows/desktop/api/iads/ns-iads-ads_object_info">ADS_OBJECT_INFO</a> structure that contains data regarding the requested directory service object. If <i>ppObjInfo</i> is <b>NULL</b> on return, <b>GetObjectInformation</b> cannot obtain the requested data.

## -returns

This method returns the standard return values, including <b>S_OK</b> when the data is obtained successfully. For more information and other return values, see  <a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>.

## -remarks

The caller should call 
the <a href="/windows/desktop/api/adshlp/nf-adshlp-freeadsmem">FreeADsMem</a> helper function to release the  <a href="/windows/desktop/api/iads/ns-iads-ads_object_info">ADS_OBJECT_INFO</a> structure created by the  <b>GetObjectInformation</b> function.

Automation clients must call  <a href="/windows/desktop/api/iads/nf-iads-iads-getinfo">IADs::GetInfo</a>.


#### Examples

The following C++ code example shows how to retrieve the object data (<a href="/windows/desktop/api/iads/ns-iads-ads_object_info">ADS_OBJECT_INFO</a>) using the <b>GetObjectInformation</b> method of an object (m_pDirObject) that implements the  <a href="/windows/desktop/api/iads/nn-iads-idirectoryobject">IDirectoryObject</a> interface.


```cpp
ADS_OBJECT_INFO *pInfo;
HRESULT hr;
 
hr = m_pDirObject->GetObjectInformation(&pInfo);
if (!SUCCEEDED(hr) )
{
   return;
}
 
//////////////////////////
// Show the attributes 
/////////////////////////
 
printf("RDN: %S\n", pInfo->pszRDN);
printf("ObjectDN: %S\n", pInfo->pszObjectDN);
printf("Parent DN: %S\n", pInfo->pszParentDN);
printf("Class Name: %S\n", pInfo->pszClassName);
printf("Schema DN: %S\n", pInfo->pszSchemaDN);
 
///////////////////////////////////////////////////////////
// Remember to clean up the memory using FreeADsMem.
//////////////////////////////////////////////////////////
FreeADsMem( pInfo );
```

## -see-also

<a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>



<a href="/windows/desktop/api/iads/ns-iads-ads_object_info">ADS_OBJECT_INFO</a>



<a href="/windows/desktop/api/iads/nf-iads-iads-getinfo">IADs::GetInfo</a>



<a href="/windows/desktop/api/iads/nn-iads-idirectoryobject">IDirectoryObject</a>