---
UID: NS:elscore._MAPPING_SERVICE_INFO
title: MAPPING_SERVICE_INFO (elscore.h)
description: Contains information about an ELS service.
helpviewer_keywords: ["*PMAPPING_SERVICE_INFO","0","1","MAPPING_SERVICE_INFO","MAPPING_SERVICE_INFO structure [Internationalization for Windows Applications]","PMAPPING_SERVICE_INFO","PMAPPING_SERVICE_INFO structure pointer [Internationalization for Windows Applications]","elscore/MAPPING_SERVICE_INFO","elscore/PMAPPING_SERVICE_INFO","intl.mappingserviceinfo"]
old-location: intl\mappingserviceinfo.htm
tech.root: Intl
ms.assetid: 444102a7-0da9-44be-989e-7a5139320034
ms.date: 12/05/2018
ms.keywords: '*PMAPPING_SERVICE_INFO, 0, 1, MAPPING_SERVICE_INFO, MAPPING_SERVICE_INFO structure [Internationalization for Windows Applications], PMAPPING_SERVICE_INFO, PMAPPING_SERVICE_INFO structure pointer [Internationalization for Windows Applications], elscore/MAPPING_SERVICE_INFO, elscore/PMAPPING_SERVICE_INFO, intl.mappingserviceinfo'
req.header: elscore.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: MAPPING_SERVICE_INFO, *PMAPPING_SERVICE_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MAPPING_SERVICE_INFO
 - elscore/_MAPPING_SERVICE_INFO
 - PMAPPING_SERVICE_INFO
 - elscore/PMAPPING_SERVICE_INFO
 - MAPPING_SERVICE_INFO
 - elscore/MAPPING_SERVICE_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Elscore.h
api_name:
 - MAPPING_SERVICE_INFO
---

# MAPPING_SERVICE_INFO structure


## -description

Contains information about an ELS service.

## -struct-fields

### -field Size

Size of the structure, used to validate the structure version. This value is required.

### -field pszCopyright

Pointer to copyright information about the service.

### -field wMajorVersion

Major version number that is used to track changes to the service.

### -field wMinorVersion

Minor version number that is used to track changes to the service.

### -field wBuildVersion

Build version that is used to track changes to the service.

### -field wStepVersion

Step version that is used to track changes to the service.

### -field dwInputContentTypesCount

Number of content types that the service can receive.

### -field prgInputContentTypes

Optional. Pointer to an array of input content types, following the format of the MIME content types, that identify the format that the service interprets when the application passes data. Examples of content types are "text/plain", "text/html" and "text/css". 

<div class="alert"><b>Note</b>  In Windows 7, the ELS services support only the content type "text/plain". A content types specification can be found at <a href="https://www.iana.org/assignments/media-types/text">Text Media Types</a>.</div>
<div> </div>

### -field dwOutputContentTypesCount

Number of content types in which the service can format results.

### -field prgOutputContentTypes

Optional. Pointer to an array of output content types, following the format of the MIME content types, that identify the format in which the service retrieves data.

### -field dwInputLanguagesCount

Number of input languages supported by the service. This member is set to 0 if the service can accept data in any language.

### -field prgInputLanguages

Pointer to an array of the input languages, following the IETF naming convention, that the service accepts. This member is set to <b>NULL</b> if the service can work with any input language.

### -field dwOutputLanguagesCount

Number of output languages supported by the service. This member is set to 0 if the service can retrieve data in any language, or if the service ignores the output language.

### -field prgOutputLanguages

Pointer to an array of output languages, following the IETF naming convention, in which the service can retrieve results. This member is set to <b>NULL</b> if the service can retrieve results in any language, or if the service ignores the output language.

### -field dwInputScriptsCount

Number of input scripts supported by the service. This member is set to 0 if the service can accept data in any script.

### -field prgInputScripts

Pointer to an array of input scripts, with Unicode standard script names, that are supported by the service. This member is set to <b>NULL</b> if the service can work with any scripts, or if the service ignores the input scripts.

### -field dwOutputScriptsCount

Number of output scripts supported by the service. This member is set to 0 if the service can retrieve data in any script, or if the service ignores the output scripts.

### -field prgOutputScripts

Pointer to an array of output scripts supported by the service. This member is set to <b>NULL</b> if the service can work with any scripts, or the service ignores the output scripts.

### -field guid

Globally unique identifier (GUID) for the service.

### -field pszCategory

Pointer to the service category for the service, for example, "Language Detection".

### -field pszDescription

Pointer to the service description. This text can be localized.

### -field dwPrivateDataSize

Size, in bytes, of the private data for the service. This member is set to 0 if there is no private data.

### -field pPrivateData

Pointer to private data that the service can expose. This information is static and updated during installation of the service.

### -field pContext

Reserved for internal use.

### -field IsOneToOneLanguageMapping

Flag indicating the language mapping between input language and output language that is supported by the service. Possible values are shown in the following table.
			 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="0"></a><dl>
<dt><b>0</b></dt>
</dl>
</td>
<td width="60%">
The input and output languages are not paired and the service can receive data in any of the input languages and render data in any of the output languages.

</td>
</tr>
<tr>
<td width="40%"><a id="1"></a><dl>
<dt><b>1</b></dt>
</dl>
</td>
<td width="60%">
The arrays of the input and output languages for the service are paired. In other words, given a particular input language, the service retrieves results in the paired language defined in the output language array. Use of the language pairing can be useful, for example, in bilingual dictionary scenarios. 

</td>
</tr>
</table>

### -field HasSubservices

Flag indicating if the service has subservices, that is, other services that plug into the service. This flag is used in service enumeration to determine if the parent service must be called to get a list of subservices. Possible values are shown in the following table.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="0"></a><dl>
<dt><b>0</b></dt>
</dl>
</td>
<td width="60%">
The service is a regular service that stands alone and has no subservices. 

</td>
</tr>
<tr>
<td width="40%"><a id="1"></a><dl>
<dt><b>1</b></dt>
</dl>
</td>
<td width="60%">
The service acts as a parent for subservices.

</td>
</tr>
</table>

### -field OnlineOnly

Reserved for future use.

### -field ServiceType

Reserved for future use.

## -remarks

Structures of this type are created in an application call to <a href="/windows/desktop/api/elscore/nf-elscore-mappinggetservices">MappingGetServices</a>.

## -see-also

<a href="/windows/desktop/Intl/extended-linguistic-services-structures">Extended Linguistic Services Structures</a>



<a href="/windows/desktop/api/elscore/nf-elscore-mappinggetservices">MappingGetServices</a>