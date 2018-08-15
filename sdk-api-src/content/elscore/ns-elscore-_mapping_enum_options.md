---
UID: NS:elscore._MAPPING_ENUM_OPTIONS
title: "_MAPPING_ENUM_OPTIONS"
author: windows-sdk-content
description: Contains options used by the MappingGetServices function to enumerate ELS services.
old-location: intl\mappingenumoptions.htm
old-project: Intl
ms.assetid: 3c5a0c04-9789-48dc-bc8f-a8b5ff350e27
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PMAPPING_ENUM_OPTIONS, MAPPING_ENUM_OPTIONS, MAPPING_ENUM_OPTIONS structure [Internationalization for Windows Applications], PMAPPING_ENUM_OPTIONS, PMAPPING_ENUM_OPTIONS structure pointer [Internationalization for Windows Applications], _MAPPING_ENUM_OPTIONS, elscore/MAPPING_ENUM_OPTIONS, elscore/PMAPPING_ENUM_OPTIONS, intl.mappingenumoptions"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: elscore.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
req.typenames: MAPPING_ENUM_OPTIONS, *PMAPPING_ENUM_OPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Elscore.h
api_name:
 - MAPPING_ENUM_OPTIONS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# _MAPPING_ENUM_OPTIONS structure


## -description



Contains options used by the <a href="https://msdn.microsoft.com/6d02e085-405e-4388-bf2f-409c92a7b190">MappingGetServices</a> function to enumerate ELS services.




## -struct-fields




### -field Size

Size of the structure, used to validate the structure version. This value is required.


### -field pszCategory

Optional. Pointer to a service category, for example, "Language Detection". The application must set this member to <b>NULL</b> if the service category is not a search criterion.


### -field pszInputLanguage

Optional. Pointer to an input language string, following the IETF naming convention, that identifies the input language that services should accept. The application can set this member to <b>NULL</b> if the supported input language is not a search criterion.


### -field pszOutputLanguage

Optional. Pointer to an output language string, following the IETF naming convention, that identifies the output language that services use to retrieve results. The application can set this member to <b>NULL</b> if the output language is not a search criterion.


### -field pszInputScript

Optional. Pointer to a standard Unicode script name that can be accepted by services. The application set this member to <b>NULL</b> if the input script is not a search criterion.


### -field pszOutputScript

Optional. Pointer to a standard Unicode script name used by services. The application can set this member to <b>NULL</b> if the output script is not a search criterion.


### -field pszInputContentType

Optional. Pointer to a string, following the format of the MIME content types, that identifies the format that the services should be able to interpret when the application passes data. Examples of content types are "text/plain", "text/html", and "text/css". The application can set this member to <b>NULL</b> if the input content type is not a search criterion. 

<div class="alert"><b>Note</b>  In Windows 7, the ELS services support only the content type "text/plain". A content type specification can be found at <a href="http://go.microsoft.com/fwlink/p/?linkid=161570">Text Media Types</a>.</div>
<div> </div>

### -field pszOutputContentType

Optional. Pointer to a string, following the format of the MIME content types, that identifies the format in which the services retrieve data. The application can set this member to <b>NULL</b> if the output content type is not a search criterion.


### -field pGuid

Optional. Pointer to a globally unique identifier (GUID) structure for a specific service. The application must set this member to <b>NULL</b> if the GUID is not a search criterion.


### -field OnlineService

Reserved for future use. Must be set to 0.


### -field ServiceType

Reserved for future use. Must be set to 0.


## -remarks



The <b>Size</b> member is the only required member of this structure. All the other members are optional. The application can set any of the members that it needs for search criteria.




## -see-also




<a href="https://msdn.microsoft.com/58cdccf8-f052-4bb3-9391-2cc537d820dd">Extended Linguistic Services Structures</a>



<a href="https://msdn.microsoft.com/6d02e085-405e-4388-bf2f-409c92a7b190">MappingGetServices</a>
 

 

