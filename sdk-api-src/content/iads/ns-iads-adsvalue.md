---
UID: NS:iads._adsvalue
title: ADSVALUE (iads.h)
description: Contains a value specified as an ADSI data type.
helpviewer_keywords: ["*LPADSVALUE","*PADSVALUE","ADSVALUE","ADSVALUE structure [ADSI]","LPADSVALUE","LPADSVALUE structure pointer [ADSI]","PADSVALUE","PADSVALUE structure pointer [ADSI]","_ds_adsvalue","adsi.adsvalue","iads/ADSVALUE","iads/LPADSVALUE","iads/PADSVALUE"]
old-location: adsi\adsvalue.htm
tech.root: adsi
ms.assetid: b53c4a14-9965-4025-95bc-37f460ea2bc9
ms.date: 12/05/2018
ms.keywords: '*LPADSVALUE, *PADSVALUE, ADSVALUE, ADSVALUE structure [ADSI], LPADSVALUE, LPADSVALUE structure pointer [ADSI], PADSVALUE, PADSVALUE structure pointer [ADSI], _ds_adsvalue, adsi.adsvalue, iads/ADSVALUE, iads/LPADSVALUE, iads/PADSVALUE'
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
req.typenames: ADSVALUE, *PADSVALUE, *LPADSVALUE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _adsvalue
 - iads/_adsvalue
 - PADSVALUE
 - iads/PADSVALUE
 - ADSVALUE
 - iads/ADSVALUE
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
 - ADSVALUE
---

# ADSVALUE structure


## -description

The <b>ADSVALUE</b> structure contains a value specified as an ADSI data type. These data types can be  <a href="/windows/desktop/ADSI/adsi-simple-data-types">ADSI Simple Data Types</a> or ADSI-defined custom data types that include C-style structures.

The <a href="/windows/desktop/api/iads/ns-iads-ads_attr_info">ADS_ATTR_INFO</a> structure contains an array of <b>ADSVALUE</b> structures. Each <b>ADSVALUE</b> structure contains a single attribute value.

## -struct-fields

### -field dwType

Data type used to interpret the union member of the structure. Values of this member are taken from the  <a href="/windows/win32/api/iads/ne-iads-adstypeenum">ADSTYPEENUM</a> enumeration.

### -field DNString

The null-terminated Unicode string that identifies the distinguished name (path) of a directory service object, as defined by <b>ADS_DN_STRING</b>, an  <a href="/windows/desktop/ADSI/adsi-simple-data-types">ADSI simple data type</a>.

### -field CaseExactString

The null-terminated Unicode string to be interpreted case-sensitively, as defined by <b>ADS_CASE_EXACT_STRING</b>, an  <a href="/windows/desktop/ADSI/adsi-simple-data-types">ADSI simple data type</a>.

### -field CaseIgnoreString

The null-terminated Unicode string to be interpreted without regard to case, as defined by <b>ADS_CASE_IGNORE_STRING</b>, an  <a href="/windows/desktop/ADSI/adsi-simple-data-types">ADSI simple data type</a>.

### -field PrintableString

The null-terminated Unicode string that can be displayed or printed, as defined by <b>ADS_PRINTABLE_STRING</b>, an  <a href="/windows/desktop/ADSI/adsi-simple-data-types">ADSI simple data type</a>.

### -field NumericString

The null-terminated Unicode string that contains numerals to be interpreted as text, as defined by <b>ADS_NUMERIC_STRING</b>, an  <a href="/windows/desktop/ADSI/adsi-simple-data-types">ADSI simple data type</a>.

### -field Boolean

Boolean value, as defined by <b>ADS_BOOLEAN</b>, an  <a href="/windows/desktop/ADSI/adsi-simple-data-types">ADSI simple data type</a>.

### -field Integer

Integer value, as defined by <b>ADS_INTEGER</b>, an  <a href="/windows/desktop/ADSI/adsi-simple-data-types">ADSI simple data type</a>.

### -field OctetString

An octet string, as defined by  <a href="/windows/win32/api/iads/ns-iads-ads_octet_string">ADS_OCTET_STRING</a>, an ADSI-defined data type.

### -field UTCTime

Time specified as Coordinated Universal Time (UTC), as defined by <b>ADS_UTC_TIME</b>, an  <a href="/windows/desktop/ADSI/adsi-simple-data-types">ADSI simple data type</a>.

### -field LargeInteger

Long integer value, as defined by <b>ADS_LARGE_INTEGER</b>, an  <a href="/windows/desktop/ADSI/adsi-simple-data-types">ADSI simple data type</a>.

### -field ClassName

Class name string, as defined by <b>ADS_OBJECT_CLASS</b>, an  <a href="/windows/desktop/ADSI/adsi-simple-data-types">ADSI simple data type</a>.

### -field ProviderSpecific

Provider-specific structure, as defined by  <a href="/windows/win32/api/iads/ns-iads-ads_prov_specific">ADS_PROV_SPECIFIC</a>, an ADSI-defined data type.

### -field pCaseIgnoreList

Pointer to a  <a href="/windows/desktop/api/iads/ns-iads-ads_caseignore_list">ADS_CASEIGNORE_LIST</a>, an ADSI-defined data type.

### -field pOctetList

Pointer to a list of  <a href="/windows/desktop/api/iads/ns-iads-ads_octet_list">ADS_OCTET_LIST</a>, an ADSI-defined data type.

### -field pPath

Pointer to the  <a href="/windows/win32/api/iads/ns-iads-ads_path">ADS_PATH</a> name, an ADSI-defined data type.

### -field pPostalAddress

Pointer to the  <a href="/windows/win32/api/iads/ns-iads-ads_postaladdress">ADS_POSTALADDRESS</a> data, an ADSI-defined data type.

### -field Timestamp

Time stamp of the  <a href="/windows/win32/api/iads/ns-iads-ads_timestamp">ADS_TIMESTAMP</a> type, an ADSI-defined data type.

### -field BackLink

A link of the  <a href="/windows/win32/api/iads/ns-iads-ads_backlink">ADS_BACKLINK</a> type, an ADSI-defined data type.

### -field pTypedName

Pointer to the  <a href="/windows/win32/api/iads/ns-iads-ads_typedname">ADS_TYPEDNAME</a> name, an ADSI-defined data type.

### -field Hold

A data structure of the  <a href="/windows/win32/api/iads/ns-iads-ads_hold">ADS_HOLD</a> type, an ADSI-defined data type.

### -field pNetAddress

Pointer to the  <a href="/windows/win32/api/iads/ns-iads-ads_netaddress">ADS_NETADDRESS</a> data, an ADSI-defined data type.

### -field pReplicaPointer

Pointer to a replica pointer of  <a href="/windows/win32/api/iads/ns-iads-ads_replicapointer">ADS_REPLICAPOINTER</a>, an ADSI-defined data type.

### -field pFaxNumber

Pointer to a facsimile number of  <a href="/windows/win32/api/iads/ns-iads-ads_faxnumber">ADS_FAXNUMBER</a>, an ADSI-defined data type.

### -field Email

Email address of a user of  <a href="/windows/win32/api/iads/ns-iads-ads_email">ADS_EMAIL</a>, an ADSI-defined data type.

### -field SecurityDescriptor

Windows security descriptor, as defined by  <a href="/windows/win32/api/iads/ns-iads-ads_nt_security_descriptor">ADS_NT_SECURITY_DESCRIPTOR</a>, an ADSI-defined data type.

### -field pDNWithBinary

Pointer to an  <a href="/windows/win32/api/iads/ns-iads-ads_dn_with_binary">ADS_DN_WITH_BINARY</a> structure that maps a distinguished name of an object to its GUID value.

### -field pDNWithString

Pointer to an  <a href="/windows/win32/api/iads/ns-iads-ads_dn_with_string">ADS_DN_WITH_STRING</a> structure that maps a distinguished name of an object to a nonvarying string value.

## -remarks

Members of the <b>ADSVALUE</b> structure specify the data type of attributes. For more information and a code example, see  <a href="/windows/desktop/api/iads/ns-iads-ads_attr_info">ADS_ATTR_INFO</a>.

## -see-also

<a href="/windows/desktop/ADSI/adsi-simple-data-types">ADSI Simple Data
  Types</a>



<a href="/windows/desktop/ADSI/adsi-structures">ADSI Structures</a>



<a href="/windows/win32/api/iads/ne-iads-adstypeenum">ADSTYPEENUM</a>



<a href="/windows/desktop/api/iads/ns-iads-ads_attr_info">ADS_ATTR_INFO</a>



<a href="/windows/win32/api/iads/ns-iads-ads_backlink">ADS_BACKLINK</a>



<a href="/windows/desktop/api/iads/ns-iads-ads_caseignore_list">ADS_CASEIGNORE_LIST</a>



<a href="/windows/win32/api/iads/ns-iads-ads_dn_with_binary">ADS_DN_WITH_BINARY</a>



<a href="/windows/win32/api/iads/ns-iads-ads_dn_with_string">ADS_DN_WITH_STRING</a>



<a href="/windows/win32/api/iads/ns-iads-ads_email">ADS_EMAIL</a>



<a href="/windows/win32/api/iads/ns-iads-ads_faxnumber">ADS_FAXNUMBER</a>



<a href="/windows/win32/api/iads/ns-iads-ads_hold">ADS_HOLD</a>



<a href="/windows/win32/api/iads/ns-iads-ads_netaddress">ADS_NETADDRESS</a>



<a href="/windows/win32/api/iads/ns-iads-ads_nt_security_descriptor">ADS_NT_SECURITY_DESCRIPTOR</a>



<a href="/windows/desktop/api/iads/ns-iads-ads_octet_list">ADS_OCTET_LIST</a>



<a href="/windows/win32/api/iads/ns-iads-ads_octet_string">ADS_OCTET_STRING</a>



<a href="/windows/win32/api/iads/ns-iads-ads_path">ADS_PATH</a>



<a href="/windows/win32/api/iads/ns-iads-ads_postaladdress">ADS_POSTALADDRESS</a>



<a href="/windows/win32/api/iads/ns-iads-ads_prov_specific">ADS_PROV_SPECIFIC</a>



<a href="/windows/win32/api/iads/ns-iads-ads_replicapointer">ADS_REPLICAPOINTER</a>



<a href="/windows/win32/api/iads/ns-iads-ads_timestamp">ADS_TIMESTAMP</a>



<a href="/windows/win32/api/iads/ns-iads-ads_typedname">ADS_TYPEDNAME</a>



<a href="/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject">IDirectoryObject::CreateDSObject</a>



<a href="/windows/desktop/api/iads/nf-iads-idirectoryobject-getobjectattributes">IDirectoryObject::GetObjectAttributes</a>



<a href="/windows/desktop/api/iads/nf-iads-idirectoryobject-setobjectattributes">IDirectoryObject::SetObjectAttributes</a>



<a href="/windows/desktop/api/iads/nf-iads-idirectorysearch-setsearchpreference">IDirectorySearch::SetSearchPreference</a>