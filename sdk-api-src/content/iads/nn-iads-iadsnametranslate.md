---
UID: NN:iads.IADsNameTranslate
title: IADsNameTranslate (iads.h)
description: The IADsNameTranslateinterface translates distinguished names (DNs) among various formats as defined in the ADS_NAME_TYPE_ENUM enumeration. The feature is available to objects in Active Directory.
helpviewer_keywords: ["IADsNameTranslate","IADsNameTranslate interface [ADSI]","IADsNameTranslate interface [ADSI]","described","NameTranslate","_ds_iadsnametranslate","adsi.iadsnametranslate","iads/IADsNameTranslate"]
old-location: adsi\iadsnametranslate.htm
tech.root: adsi
ms.assetid: 3d8baeb1-0edc-4648-8691-6ea4dcfd8f62
ms.date: 12/05/2018
ms.keywords: IADsNameTranslate, IADsNameTranslate interface [ADSI], IADsNameTranslate interface [ADSI],described, NameTranslate, _ds_iadsnametranslate, adsi.iadsnametranslate, iads/IADsNameTranslate
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
 - IADsNameTranslate
 - iads/IADsNameTranslate
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
 - IADsNameTranslate
 - NameTranslate
---

# IADsNameTranslate interface


## -description

The <b>IADsNameTranslate</b> interface translates distinguished names (DNs) among various
  formats as defined in the 
   <a href="/windows/win32/api/iads/ne-iads-ads_name_type_enum">ADS_NAME_TYPE_ENUM</a> enumeration.
  The feature is available to objects in Active Directory.

Name
  translations are performed on the directory server. To translate a DN, communicate with the server by means of an <b>IADsNameTranslate</b> object, and specify which object is of interest
  and what format is desired. The following is the general process for using the
  <b>IADsNameTranslate</b> interface.

First, create an instance of the <b>IADsNameTranslate</b> object.

Second, initialize the <b>IADsNameTranslate</b> object by specifying the directory server using the  
     <a href="/windows/desktop/api/iads/nf-iads-iadsnametranslate-init">IADsNameTranslate::Init</a> or 
     <a href="/windows/desktop/api/iads/nf-iads-iadsnametranslate-initex">IADsNameTranslate::InitEx</a> methods.

Third, set the directory object on the server by specifying the name with the <a href="/windows/desktop/api/iads/nf-iads-iadsnametranslate-set">IADsNameTranslate::Set</a> method and the format with the <a href="/windows/desktop/api/iads/nf-iads-iadsnametranslate-setex">IADsNameTranslate::SetEx</a> method.

Fourth, retrieve the object name in the specified format with the <a href="/windows/desktop/api/iads/nf-iads-iadsnametranslate-get">IADsNameTranslate::Get</a> or 
     <a href="/windows/desktop/api/iads/nf-iads-iadsnametranslate-getex">IADsNameTranslate::GetEx</a> method.

The following code example shows how to create an <b>IADsNameTranslate</b> object in Visual C++, Visual Basic, and
  VBScript/Active Server Pages.
<div class="alert"><b>Note</b>  The format elements as defined in the <a href="/windows/win32/api/iads/ne-iads-ads_name_type_enum">ADS_NAME_TYPE_ENUM</a> enumeration and used
  by <b>IADsNameTranslate</b> are not equivalent and are 
  non-interchangeable with the format elements used by the
  <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dscracknamesa">DsCrackName</a> function. Do not confuse the proper use of these similarly named but non-interchangeable element
  formats.</div><div> </div>

## -inheritance

The <b>IADsNameTranslate</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IADsNameTranslate</b> also has these types of members:

## -see-also

<a href="/windows/win32/api/iads/ne-iads-ads_name_type_enum">ADS_NAME_TYPE_ENUM</a>



<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a>



<a href="/windows/desktop/ADSI/iadsnametranslate-property-methods">IADsNameTranslate
    Property Methods</a>



<a href="/windows/desktop/ADSI/iadsnametranslate-interface">IADsNameTranslate Interface</a>



<a href="/windows/desktop/api/iads/nf-iads-iadsnametranslate-get">IADsNameTranslate::Get</a>



<a href="/windows/desktop/api/iads/nf-iads-iadsnametranslate-getex">IADsNameTranslate::GetEx</a>



<a href="/windows/desktop/api/iads/nf-iads-iadsnametranslate-init">IADsNameTranslate::Init</a>



<a href="/windows/desktop/api/iads/nf-iads-iadsnametranslate-initex">IADsNameTranslate::InitEx</a>



<a href="/windows/desktop/api/iads/nf-iads-iadsnametranslate-set">IADsNameTranslate::Set</a>



<a href="/windows/desktop/api/iads/nf-iads-iadsnametranslate-setex">IADsNameTranslate::SetEx</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
