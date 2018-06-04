---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _adsvalue structure


## -description


The <b>ADSVALUE</b> structure contains a value specified as an ADSI data type. These data types can be  <a href="https://msdn.microsoft.com/0bd34f13-269f-4f5d-8a18-74577522e402">ADSI Simple Data Types</a> or ADSI-defined custom data types that include C-style structures.

The <a href="https://msdn.microsoft.com/a2b97a52-4b8b-4491-8798-72a161903422">ADS_ATTR_INFO</a> structure contains an array of <b>ADSVALUE</b> structures. Each <b>ADSVALUE</b> structure contains a single attribute value.


## -struct-fields




### -field dwType

Data type used to interpret the union member of the structure. Values of this member are taken from the  <a href="https://msdn.microsoft.com/e601bae5-80bf-43f5-846f-11327889419a">ADSTYPEENUM</a> enumeration.


### -field DNString

The null-terminated Unicode string that identifies the distinguished name (path) of a directory service object, as defined by <b>ADS_DN_STRING</b>, an  <a href="https://msdn.microsoft.com/0bd34f13-269f-4f5d-8a18-74577522e402">ADSI simple data type</a>.


### -field CaseExactString

The null-terminated Unicode string to be interpreted case-sensitively, as defined by <b>ADS_CASE_EXACT_STRING</b>, an  <a href="https://msdn.microsoft.com/0bd34f13-269f-4f5d-8a18-74577522e402">ADSI simple data type</a>.


### -field CaseIgnoreString

The null-terminated Unicode string to be interpreted without regard to case, as defined by <b>ADS_CASE_IGNORE_STRING</b>, an  <a href="https://msdn.microsoft.com/0bd34f13-269f-4f5d-8a18-74577522e402">ADSI simple data type</a>.


### -field PrintableString

The null-terminated Unicode string that can be displayed or printed, as defined by <b>ADS_PRINTABLE_STRING</b>, an  <a href="https://msdn.microsoft.com/0bd34f13-269f-4f5d-8a18-74577522e402">ADSI simple data type</a>.


### -field NumericString

The null-terminated Unicode string that contains numerals to be interpreted as text, as defined by <b>ADS_NUMERIC_STRING</b>, an  <a href="https://msdn.microsoft.com/0bd34f13-269f-4f5d-8a18-74577522e402">ADSI simple data type</a>.


### -field Boolean

Boolean value, as defined by <b>ADS_BOOLEAN</b>, an  <a href="https://msdn.microsoft.com/0bd34f13-269f-4f5d-8a18-74577522e402">ADSI simple data type</a>.


### -field Integer

Integer value, as defined by <b>ADS_INTEGER</b>, an  <a href="https://msdn.microsoft.com/0bd34f13-269f-4f5d-8a18-74577522e402">ADSI simple data type</a>.


### -field OctetString

An octet string, as defined by  <a href="https://msdn.microsoft.com/ecad3601-081d-4cb6-a6dd-7781d652af8e">ADS_OCTET_STRING</a>, an ADSI-defined data type.


### -field UTCTime

Time specified as Coordinated Universal Time (UTC), as defined by <b>ADS_UTC_TIME</b>, an  <a href="https://msdn.microsoft.com/0bd34f13-269f-4f5d-8a18-74577522e402">ADSI simple data type</a>.


### -field LargeInteger

Long integer value, as defined by <b>ADS_LARGE_INTEGER</b>, an  <a href="https://msdn.microsoft.com/0bd34f13-269f-4f5d-8a18-74577522e402">ADSI simple data type</a>.


### -field ClassName

Class name string, as defined by <b>ADS_OBJECT_CLASS</b>, an  <a href="https://msdn.microsoft.com/0bd34f13-269f-4f5d-8a18-74577522e402">ADSI simple data type</a>.


### -field ProviderSpecific

Provider-specific structure, as defined by  <a href="https://msdn.microsoft.com/45927280-7fb5-49a6-8ecd-f0a6931bed6a">ADS_PROV_SPECIFIC</a>, an ADSI-defined data type.


### -field pCaseIgnoreList

Pointer to a  <a href="https://msdn.microsoft.com/448c4541-7478-44f3-9be3-f1200f83978a">ADS_CASEIGNORE_LIST</a>, an ADSI-defined data type.


### -field pOctetList

Pointer to a list of  <a href="https://msdn.microsoft.com/9a6a6ba8-afe1-44d3-a9a8-dab1c5f4265e">ADS_OCTET_LIST</a>, an ADSI-defined data type.


### -field pPath

Pointer to the  <a href="https://msdn.microsoft.com/b8393a81-3e2a-4e59-a6be-def779efbe82">ADS_PATH</a> name, an ADSI-defined data type.


### -field pPostalAddress

Pointer to the  <a href="https://msdn.microsoft.com/ae56f4ca-e6f1-4199-83b2-6d810d24fb4a">ADS_POSTALADDRESS</a> data, an ADSI-defined data type.


### -field Timestamp

Time stamp of the  <a href="https://msdn.microsoft.com/3e416a9a-e444-43eb-9e59-e8e91ccac2d9">ADS_TIMESTAMP</a> type, an ADSI-defined data type.


### -field BackLink

A link of the  <a href="https://msdn.microsoft.com/1352d304-b984-43ab-8c47-5108f35ae193">ADS_BACKLINK</a> type, an ADSI-defined data type.


### -field pTypedName

Pointer to the  <a href="https://msdn.microsoft.com/64ce748c-adfc-4beb-8507-ca6aece46ad0">ADS_TYPEDNAME</a> name, an ADSI-defined data type.


### -field Hold

A data structure of the  <a href="https://msdn.microsoft.com/f1ef87f0-b024-4d16-873b-a68bb62f4206">ADS_HOLD</a> type, an ADSI-defined data type.


### -field pNetAddress

Pointer to the  <a href="https://msdn.microsoft.com/108c5e24-c52b-472a-b5c6-f7d534cab892">ADS_NETADDRESS</a> data, an ADSI-defined data type.


### -field pReplicaPointer

Pointer to a replica pointer of  <a href="https://msdn.microsoft.com/f8cb8763-9533-4b80-8617-a99d75c92f07">ADS_REPLICAPOINTER</a>, an ADSI-defined data type.


### -field pFaxNumber

Pointer to a facsimile number of  <a href="https://msdn.microsoft.com/32553290-e9ca-44e7-a085-f053df8104e6">ADS_FAXNUMBER</a>, an ADSI-defined data type.


### -field Email

Email address of a user of  <a href="https://msdn.microsoft.com/72d9ed78-1ae8-456c-9f06-4284446a3234">ADS_EMAIL</a>, an ADSI-defined data type.


### -field SecurityDescriptor

Windows security descriptor, as defined by  <a href="https://msdn.microsoft.com/4776fe35-2c16-4dd3-b708-cf36e2423425">ADS_NT_SECURITY_DESCRIPTOR</a>, an ADSI-defined data type.


### -field pDNWithBinary

Pointer to an  <a href="https://msdn.microsoft.com/541dd19d-79a1-4a74-b4a1-31cdf69fbf0c">ADS_DN_WITH_BINARY</a> structure that maps a distinguished name of an object to its GUID value.


### -field pDNWithString

Pointer to an  <a href="https://msdn.microsoft.com/715354fe-1e62-4fbd-a5ba-0d7a56b83390">ADS_DN_WITH_STRING</a> structure that maps a distinguished name of an object to a nonvarying string value.


## -remarks



Members of the <b>ADSVALUE</b> structure specify the data type of attributes. For more information and a code example, see  <a href="https://msdn.microsoft.com/a2b97a52-4b8b-4491-8798-72a161903422">ADS_ATTR_INFO</a>.




## -see-also




<a href="https://msdn.microsoft.com/0bd34f13-269f-4f5d-8a18-74577522e402">ADSI Simple Data
  Types</a>



<a href="https://msdn.microsoft.com/3ee0e469-9932-4135-8798-27d318011786">ADSI Structures</a>



<a href="https://msdn.microsoft.com/e601bae5-80bf-43f5-846f-11327889419a">ADSTYPEENUM</a>



<a href="https://msdn.microsoft.com/a2b97a52-4b8b-4491-8798-72a161903422">ADS_ATTR_INFO</a>



<a href="https://msdn.microsoft.com/1352d304-b984-43ab-8c47-5108f35ae193">ADS_BACKLINK</a>



<a href="https://msdn.microsoft.com/448c4541-7478-44f3-9be3-f1200f83978a">ADS_CASEIGNORE_LIST</a>



<a href="https://msdn.microsoft.com/541dd19d-79a1-4a74-b4a1-31cdf69fbf0c">ADS_DN_WITH_BINARY</a>



<a href="https://msdn.microsoft.com/715354fe-1e62-4fbd-a5ba-0d7a56b83390">ADS_DN_WITH_STRING</a>



<a href="https://msdn.microsoft.com/72d9ed78-1ae8-456c-9f06-4284446a3234">ADS_EMAIL</a>



<a href="https://msdn.microsoft.com/32553290-e9ca-44e7-a085-f053df8104e6">ADS_FAXNUMBER</a>



<a href="https://msdn.microsoft.com/f1ef87f0-b024-4d16-873b-a68bb62f4206">ADS_HOLD</a>



<a href="https://msdn.microsoft.com/108c5e24-c52b-472a-b5c6-f7d534cab892">ADS_NETADDRESS</a>



<a href="https://msdn.microsoft.com/4776fe35-2c16-4dd3-b708-cf36e2423425">ADS_NT_SECURITY_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/9a6a6ba8-afe1-44d3-a9a8-dab1c5f4265e">ADS_OCTET_LIST</a>



<a href="https://msdn.microsoft.com/ecad3601-081d-4cb6-a6dd-7781d652af8e">ADS_OCTET_STRING</a>



<a href="https://msdn.microsoft.com/b8393a81-3e2a-4e59-a6be-def779efbe82">ADS_PATH</a>



<a href="https://msdn.microsoft.com/ae56f4ca-e6f1-4199-83b2-6d810d24fb4a">ADS_POSTALADDRESS</a>



<a href="https://msdn.microsoft.com/45927280-7fb5-49a6-8ecd-f0a6931bed6a">ADS_PROV_SPECIFIC</a>



<a href="https://msdn.microsoft.com/f8cb8763-9533-4b80-8617-a99d75c92f07">ADS_REPLICAPOINTER</a>



<a href="https://msdn.microsoft.com/3e416a9a-e444-43eb-9e59-e8e91ccac2d9">ADS_TIMESTAMP</a>



<a href="https://msdn.microsoft.com/64ce748c-adfc-4beb-8507-ca6aece46ad0">ADS_TYPEDNAME</a>



<a href="https://msdn.microsoft.com/77648d1c-b05b-4c36-a2e3-25bb5713d615">IDirectoryObject::CreateDSObject</a>



<a href="https://msdn.microsoft.com/6e3d046f-eac0-4955-925b-71ab15df9ed3">IDirectoryObject::GetObjectAttributes</a>



<a href="https://msdn.microsoft.com/999e6766-52cf-4087-bb17-72de487975c2">IDirectoryObject::SetObjectAttributes</a>



<a href="https://msdn.microsoft.com/1c5b3f72-6165-41ad-99d4-d68bc12ac10b">IDirectorySearch::SetSearchPreference</a>
 

 

