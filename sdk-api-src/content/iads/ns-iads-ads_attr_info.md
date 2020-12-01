---
UID: NS:iads._ads_attr_info
title: ADS_ATTR_INFO (iads.h)
description: Used to contain one or more attribute values for use with the IDirectoryObject::CreateDSObject, IDirectoryObject::GetObjectAttributes, or IDirectoryObject::SetObjectAttributes method.
helpviewer_keywords: ["*PADS_ATTR_INFO","ADS_ATTR_INFO","ADS_ATTR_INFO structure [ADSI]","PADS_ATTR_INFO","PADS_ATTR_INFO structure pointer [ADSI]","_ds_ads_attr_info","adsi.ads__attr__info","adsi.ads_attr_info","iads/ADS_ATTR_INFO","iads/PADS_ATTR_INFO"]
old-location: adsi\ads_attr_info.htm
tech.root: adsi
ms.assetid: a2b97a52-4b8b-4491-8798-72a161903422
ms.date: 12/05/2018
ms.keywords: '*PADS_ATTR_INFO, ADS_ATTR_INFO, ADS_ATTR_INFO structure [ADSI], PADS_ATTR_INFO, PADS_ATTR_INFO structure pointer [ADSI], _ds_ads_attr_info, adsi.ads__attr__info, adsi.ads_attr_info, iads/ADS_ATTR_INFO, iads/PADS_ATTR_INFO'
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: ADS_ATTR_INFO, *PADS_ATTR_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _ads_attr_info
 - iads/_ads_attr_info
 - PADS_ATTR_INFO
 - iads/PADS_ATTR_INFO
 - ADS_ATTR_INFO
 - iads/ADS_ATTR_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iads.h
api_name:
 - ADS_ATTR_INFO
---

# ADS_ATTR_INFO structure


## -description

The <b>ADS_ATTR_INFO</b> structure is used to contain one or more attribute values for use with the <a href="/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject">IDirectoryObject::CreateDSObject</a>,
   <a href="/windows/desktop/api/iads/nf-iads-idirectoryobject-getobjectattributes">IDirectoryObject::GetObjectAttributes</a>, or 
   <a href="/windows/desktop/api/iads/nf-iads-idirectoryobject-setobjectattributes">IDirectoryObject::SetObjectAttributes</a> method.

## -struct-fields

### -field pszAttrName

The null-terminated Unicode string that contains the attribute name.

### -field dwControlCode

Contains one of the <a href="/windows/desktop/ADSI/adsi-attribute-modification-types">ADSI Attribute Modification Types</a> values that determines the type of operation to be performed on the attribute value.

### -field dwADsType

A value from the  <a href="/windows/win32/api/iads/ne-iads-adstypeenum">ADSTYPEENUM</a> enumeration that indicates the data type of the attribute.

### -field pADsValues

Pointer to an array of  <a href="/windows/desktop/api/iads/ns-iads-adsvalue">ADSVALUE</a> structures that contain values for the attribute.

### -field dwNumValues

Size of the <b>pADsValues</b> array.

## -remarks

In ADSI, attributes and properties are used interchangeably. Set attributes, when creating a directory service object, using the  <a href="/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject">IDirectoryObject::CreateDSObject</a> method. The  <a href="/windows/desktop/api/iads/nn-iads-idirectoryobject">IDirectoryObject</a> interface also supports the  <a href="/windows/desktop/api/iads/nf-iads-idirectoryobject-getobjectattributes">IDirectoryObject::GetObjectAttributes</a> and  <a href="/windows/desktop/api/iads/nf-iads-idirectoryobject-setobjectattributes">IDirectoryObject::SetObjectAttributes</a> methods for retrieving and modifying the attributes of the object in a directory.

Memory for the array of <a href="/windows/desktop/api/iads/ns-iads-adsvalue">ADSVALUE</a> structures is not allocated with this structure.

The value of the <b>dwControlCode</b> member is ignored when the structure is used as an OUT parameter.

## -see-also

<a href="/windows/desktop/ADSI/adsi-attribute-modification-types">ADSI Attribute Modification Types</a>



<a href="/windows/desktop/ADSI/adsi-constants">ADSI Constants</a>



<a href="/windows/desktop/ADSI/adsi-structures">ADSI Structures</a>



<a href="/windows/win32/api/iads/ne-iads-adstypeenum">ADSTYPEENUM</a>



<a href="/windows/desktop/api/iads/nn-iads-idirectoryobject">IDirectoryObject</a>



<a href="/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject">IDirectoryObject::CreateDSObject</a>



<a href="/windows/desktop/api/iads/nf-iads-idirectoryobject-getobjectattributes">IDirectoryObject::GetObjectAttributes</a>



<a href="/windows/desktop/api/iads/nf-iads-idirectoryobject-setobjectattributes">IDirectoryObject::SetObjectAttributes</a>