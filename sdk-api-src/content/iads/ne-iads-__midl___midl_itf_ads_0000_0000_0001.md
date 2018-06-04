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

# __MIDL___MIDL_itf_ads_0000_0000_0001 enumeration


## -description


The <b>ADSTYPEENUM</b> enumeration is used to identify the data type of an ADSI property value.


## -enum-fields




### -field ADSTYPE_INVALID

The data type is not valid


### -field ADSTYPE_DN_STRING

The string is of Distinguished Name (path) of a directory service object.


### -field ADSTYPE_CASE_EXACT_STRING

The string is of the case-sensitive type.


### -field ADSTYPE_CASE_IGNORE_STRING

The string is of the case-insensitive type.


### -field ADSTYPE_PRINTABLE_STRING

The string is displayable on screen or in print.


### -field ADSTYPE_NUMERIC_STRING

The string is of a numeral to be interpreted as text.


### -field ADSTYPE_BOOLEAN

The data is of a Boolean value.


### -field ADSTYPE_INTEGER

The data is of an integer value.


### -field ADSTYPE_OCTET_STRING

The string is of a byte array.


### -field ADSTYPE_UTC_TIME

The data is of the universal time as expressed in Universal Time Coordinate (UTC).


### -field ADSTYPE_LARGE_INTEGER

The data is of a long integer value.


### -field ADSTYPE_PROV_SPECIFIC

The string is of a provider-specific string.


### -field ADSTYPE_OBJECT_CLASS

Not used.


### -field ADSTYPE_CASEIGNORE_LIST

The data is of a list of case insensitive strings.


### -field ADSTYPE_OCTET_LIST

The data is of a list of octet strings.


### -field ADSTYPE_PATH

The string is of a directory path.


### -field ADSTYPE_POSTALADDRESS

The string is of the postal address type.


### -field ADSTYPE_TIMESTAMP

The data is of a time stamp in seconds.


### -field ADSTYPE_BACKLINK

The string is of a back link.


### -field ADSTYPE_TYPEDNAME

The string is of a typed name.


### -field ADSTYPE_HOLD

The data is of the Hold data structure.


### -field ADSTYPE_NETADDRESS

The string is of a net address.


### -field ADSTYPE_REPLICAPOINTER

The data is of a replica pointer.


### -field ADSTYPE_FAXNUMBER

The string is of a fax number.


### -field ADSTYPE_EMAIL

The data is of an email message.


### -field ADSTYPE_NT_SECURITY_DESCRIPTOR

The data is a Windows security descriptor as represented by a byte array.


### -field ADSTYPE_UNKNOWN

The data is of an undefined type.


### -field ADSTYPE_DN_WITH_BINARY

The data is of <a href="https://msdn.microsoft.com/541dd19d-79a1-4a74-b4a1-31cdf69fbf0c">ADS_DN_WITH_BINARY</a> used for mapping a distinguished name to a nonvarying GUID. For more information, see Remarks.


### -field ADSTYPE_DN_WITH_STRING

The data is of <a href="https://msdn.microsoft.com/715354fe-1e62-4fbd-a5ba-0d7a56b83390">ADS_DN_WITH_STRING</a> used for mapping a distinguished name to a nonvarying string value. For more information, see Remarks.


## -remarks



When extending the active directory schema to add <a href="https://msdn.microsoft.com/541dd19d-79a1-4a74-b4a1-31cdf69fbf0c">ADS_DN_WITH_BINARY</a>, you must also specify the "otherWellKnownGuid" attribute definition. Add the following to the ldf file attribute definition: "omObjectClass:: KoZIhvcUAQEBCw=="

When extending the active directory schema to add <a href="https://msdn.microsoft.com/715354fe-1e62-4fbd-a5ba-0d7a56b83390">ADS_DN_WITH_STRING</a>, you must also specify the "otherWellKnownGuid" attribute definition. Add the following to the ldf file attribute definition: "omObjectClass:: KoZIhvcUAQEBDA=="

Because VBScript cannot read data from a type library, VBScript applications do not recognize symbolic constants, as defined above. Use the numerical constants instead to set the appropriate flags in your VBScript application. To use the symbolic constants as a good programming practice, write explicit declarations of such constants, as done here, in your VBScript application.




## -see-also




<a href="https://msdn.microsoft.com/f0ad5ce5-742d-40dc-ac5a-31d779e40bfd">ADSI Enumerations</a>
 

 

