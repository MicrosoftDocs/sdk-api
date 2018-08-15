---
UID: NS:iads._ads_object_info
title: "_ads_object_info"
author: windows-sdk-content
description: The ADS_OBJECT_INFO structure specifies the data, including the identity and location, of a directory service object.
old-location: adsi\ads_object_info.htm
old-project: ADSI
ms.assetid: f072b2f8-8c03-4f90-8edf-cf5fed97a222
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: "*PADS_OBJECT_INFO, ADS_OBJECT_INFO, ADS_OBJECT_INFO structure [ADSI], PADS_OBJECT_INFO, PADS_OBJECT_INFO structure pointer [ADSI], _ads_object_info, _ds_ads_object_info, adsi.ads__object__info, adsi.ads_object_info, iads/ADS_OBJECT_INFO, iads/PADS_OBJECT_INFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: iads.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: ADS_OBJECT_INFO, *PADS_OBJECT_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iads.h
api_name:
 - ADS_OBJECT_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _ads_object_info structure


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



To obtain the object data, non-Automation clients call the  <a href="https://msdn.microsoft.com/5a2d7fee-666e-4b3b-b6fa-b9f6d785c2c1">IDirectoryObject::GetObjectInformation</a> method, which takes an out parameter, a pointer to an <b>ADS_OBJECT_INFO</b> structure allocated in the heap. Automation clients can accomplish the same task by calling  <a href="https://msdn.microsoft.com/73ceaeb1-9a6b-449a-9851-3756736dbad7">IADs::GetInfo</a>.




## -see-also




<a href="https://msdn.microsoft.com/3ee0e469-9932-4135-8798-27d318011786">ADSI Structures</a>



<a href="https://msdn.microsoft.com/73ceaeb1-9a6b-449a-9851-3756736dbad7">IADs::GetInfo</a>



<a href="https://msdn.microsoft.com/5a2d7fee-666e-4b3b-b6fa-b9f6d785c2c1">IDirectoryObject::GetObjectInformation</a>
 

 

