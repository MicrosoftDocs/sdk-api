---
UID: NS:iads._ads_attr_info
title: "_ads_attr_info"
author: windows-sdk-content
description: Used to contain one or more attribute values for use with the IDirectoryObject::CreateDSObject, IDirectoryObject::GetObjectAttributes, or IDirectoryObject::SetObjectAttributes method.
old-location: adsi\ads_attr_info.htm
old-project: ADSI
ms.assetid: a2b97a52-4b8b-4491-8798-72a161903422
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: "*PADS_ATTR_INFO, ADS_ATTR_INFO, ADS_ATTR_INFO structure [ADSI], PADS_ATTR_INFO, PADS_ATTR_INFO structure pointer [ADSI], _ads_attr_info, _ds_ads_attr_info, adsi.ads__attr__info, adsi.ads_attr_info, iads/ADS_ATTR_INFO, iads/PADS_ATTR_INFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
req.typenames: ADS_ATTR_INFO, *PADS_ATTR_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Iads.h
api_name:
-	ADS_ATTR_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _ads_attr_info structure


## -description


The <b>ADS_ATTR_INFO</b> structure is used to contain one or more attribute values for use with the <a href="https://msdn.microsoft.com/77648d1c-b05b-4c36-a2e3-25bb5713d615">IDirectoryObject::CreateDSObject</a>,
   <a href="https://msdn.microsoft.com/6e3d046f-eac0-4955-925b-71ab15df9ed3">IDirectoryObject::GetObjectAttributes</a>, or 
   <a href="https://msdn.microsoft.com/999e6766-52cf-4087-bb17-72de487975c2">IDirectoryObject::SetObjectAttributes</a> method.


## -struct-fields




### -field pszAttrName

The null-terminated Unicode string that contains the attribute name.


### -field dwControlCode

Contains one of the <a href="https://msdn.microsoft.com/e9a454c8-e067-4730-97f4-85c4f5889e05">ADSI Attribute Modification Types</a> values that determines the type of operation to be performed on the attribute value.


### -field dwADsType

A value from the  <a href="https://msdn.microsoft.com/e601bae5-80bf-43f5-846f-11327889419a">ADSTYPEENUM</a> enumeration that indicates the data type of the attribute.


### -field pADsValues

Pointer to an array of  <a href="https://msdn.microsoft.com/b53c4a14-9965-4025-95bc-37f460ea2bc9">ADSVALUE</a> structures that contain values for the attribute.


### -field dwNumValues

Size of the <b>pADsValues</b> array.


## -remarks



In ADSI, attributes and properties are used interchangeably. Set attributes, when creating a directory service object, using the  <a href="https://msdn.microsoft.com/77648d1c-b05b-4c36-a2e3-25bb5713d615">IDirectoryObject::CreateDSObject</a> method. The  <a href="https://msdn.microsoft.com/bc4f8920-2881-4393-bb01-ed837c3db6ad">IDirectoryObject</a> interface also supports the  <a href="https://msdn.microsoft.com/6e3d046f-eac0-4955-925b-71ab15df9ed3">IDirectoryObject::GetObjectAttributes</a> and  <a href="https://msdn.microsoft.com/999e6766-52cf-4087-bb17-72de487975c2">IDirectoryObject::SetObjectAttributes</a> methods for retrieving and modifying the attributes of the object in a directory.

Memory for the array of <a href="https://msdn.microsoft.com/b53c4a14-9965-4025-95bc-37f460ea2bc9">ADSVALUE</a> structures is not allocated with this structure.

The value of the <b>dwControlCode</b> member is ignored when the structure is used as an OUT parameter.




## -see-also




<a href="https://msdn.microsoft.com/e9a454c8-e067-4730-97f4-85c4f5889e05">ADSI Attribute Modification Types</a>



<a href="https://msdn.microsoft.com/facc00e8-2ecd-4428-bddd-cfa1ff1b8538">ADSI Constants</a>



<a href="https://msdn.microsoft.com/3ee0e469-9932-4135-8798-27d318011786">ADSI Structures</a>



<a href="https://msdn.microsoft.com/e601bae5-80bf-43f5-846f-11327889419a">ADSTYPEENUM</a>



<a href="https://msdn.microsoft.com/bc4f8920-2881-4393-bb01-ed837c3db6ad">IDirectoryObject</a>



<a href="https://msdn.microsoft.com/77648d1c-b05b-4c36-a2e3-25bb5713d615">IDirectoryObject::CreateDSObject</a>



<a href="https://msdn.microsoft.com/6e3d046f-eac0-4955-925b-71ab15df9ed3">IDirectoryObject::GetObjectAttributes</a>



<a href="https://msdn.microsoft.com/999e6766-52cf-4087-bb17-72de487975c2">IDirectoryObject::SetObjectAttributes</a>
 

 

