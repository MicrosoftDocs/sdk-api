---
UID: NS:iads._ads_object_info
title: ADS_OBJECT_INFO (iads.h)
description: The ADS_OBJECT_INFO structure specifies the data, including the identity and location, of a directory service object.
helpviewer_keywords: ["*PADS_OBJECT_INFO","ADS_OBJECT_INFO","ADS_OBJECT_INFO structure [ADSI]","PADS_OBJECT_INFO","PADS_OBJECT_INFO structure pointer [ADSI]","_ds_ads_object_info","adsi.ads__object__info","adsi.ads_object_info","iads/ADS_OBJECT_INFO","iads/PADS_OBJECT_INFO"]
old-location: adsi\ads_object_info.htm
tech.root: adsi
ms.assetid: f072b2f8-8c03-4f90-8edf-cf5fed97a222
ms.date: 12/05/2018
ms.keywords: '*PADS_OBJECT_INFO, ADS_OBJECT_INFO, ADS_OBJECT_INFO structure [ADSI], PADS_OBJECT_INFO, PADS_OBJECT_INFO structure pointer [ADSI], _ds_ads_object_info, adsi.ads__object__info, adsi.ads_object_info, iads/ADS_OBJECT_INFO, iads/PADS_OBJECT_INFO'
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
req.typenames: ADS_OBJECT_INFO, *PADS_OBJECT_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _ads_object_info
 - iads/_ads_object_info
 - PADS_OBJECT_INFO
 - iads/PADS_OBJECT_INFO
 - ADS_OBJECT_INFO
 - iads/ADS_OBJECT_INFO
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
 - ADS_OBJECT_INFO
---

# ADS_OBJECT_INFO structure


## -description

The <b>ADS_OBJECT_INFO</b> structure specifies the data, including the identity and location, of a directory service object.

## -struct-fields

### -field pszRDN

The null-terminated Unicode string that contains the relative distinguished name of the directory service object.

### -field pszObjectDN

The null-terminated Unicode string that contains the distinguished name  of the directory service object.

### -field pszParentDN

The null-terminated Unicode string that contains the distinguished name of the parent object.

### -field pszSchemaDN

The null-terminated Unicode string that contains the distinguished name of the schema class of the object.

### -field pszClassName

The null-terminated Unicode string that contains the name of the class of which this object is an instance.

## -remarks

To obtain the object data, non-Automation clients call the  <a href="/windows/desktop/api/iads/nf-iads-idirectoryobject-getobjectinformation">IDirectoryObject::GetObjectInformation</a> method, which takes an out parameter, a pointer to an <b>ADS_OBJECT_INFO</b> structure allocated in the heap. Automation clients can accomplish the same task by calling  <a href="/windows/desktop/api/iads/nf-iads-iads-getinfo">IADs::GetInfo</a>.

## -see-also

<a href="/windows/desktop/ADSI/adsi-structures">ADSI Structures</a>



<a href="/windows/desktop/api/iads/nf-iads-iads-getinfo">IADs::GetInfo</a>



<a href="/windows/desktop/api/iads/nf-iads-idirectoryobject-getobjectinformation">IDirectoryObject::GetObjectInformation</a>