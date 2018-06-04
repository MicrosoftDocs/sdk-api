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

# __MIDL___MIDL_itf_casetup_0000_0002_0001 enumeration


## -description


The <b>CASetupProperty</b> enumeration specifies a property type for setup and configuration of a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a> (CA) role when using the <a href="https://msdn.microsoft.com/6792a0d6-d304-481d-a97b-5fb7033c7eae">ICertSrvSetup</a> interface.


## -enum-fields




### -field ENUM_SETUPPROP_INVALID

A value that specifies a property type that is not valid.


### -field ENUM_SETUPPROP_CATYPE

A <b>VT_I4</b> value that specifies a value of the <a href="https://msdn.microsoft.com/32b20317-c0ef-4896-a8c6-309e34f87c30">ENUM_CATYPES</a> enumeration.

If the computer is not joined to a domain, or the caller

is not an Enterprise or Domain administrator but is a local administrator, the default value is <b>ENUM_STANDALONE_ROOTCA</b>. If the computer is joined to a domain, the caller is an Enterprise or Domain administrator, and an enterprise root CA already exists, the default is <b>ENUM_ENTERPRISE_SUBCA</b>, or if no enterprise root CA exists, the default value is <b>ENUM_ENTERPRISE_ROOTCA</b>.


### -field ENUM_SETUPPROP_CAKEYINFORMATION

A <b>VT_DISPATCH</b> value, in the form of a <b>CCertSrvSetupKeyInformation</b>  object, that specifies the <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">private key</a> information used for a CA certificate. By default, setup generates a new key

with a 2048-bit key length for root and subordinate CAs using "Microsoft

Strong Cryptographic Provider."



### -field ENUM_SETUPPROP_INTERACTIVE

A <b>VT_BOOL</b> value that indicates whether the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider</a> (CSP) is allowed to interact with the desktop. The default is false.



### -field ENUM_SETUPPROP_CANAME

A <b>VT_BSTR</b> value that contains the common name for the CA. By default, the common 

name is <i>DomainName</i>-<i>LocalComputerName</i>-<i>CAName</i>.



### -field ENUM_SETUPPROP_CADSSUFFIX

A <b>VT_BSTR</b> value that contains the distinguished name suffix for a CA name.


### -field ENUM_SETUPPROP_VALIDITYPERIOD

A <b>VT_I4</b> value that specifies the number of units in the validity period as specified by the <b>ENUM_SETUPPROP_VALIDITYPERIODUNIT</b> property type. For a subordinate CA, the validity period is determined by the parent CA.


### -field ENUM_SETUPPROP_VALIDITYPERIODUNIT

A <b>VT_I4</b> value that specifies a value of the <a href="https://msdn.microsoft.com/1bd8c906-7e17-4d8c-93e8-8901f9104d58">ENUM_PERIOD</a> enumeration that indicates the time units of the validity period. For a subordinate CA, the validity period time unit is determined by the parent CA.


### -field ENUM_SETUPPROP_EXPIRATIONDATE

A <b>VT_BSTR</b> value that specifies the expected expiration date of the root CA certificate based on the current time, validity period, and validity period unit. For a subordinate CA, the expiration date is

determined by its parent CA.



### -field ENUM_SETUPPROP_PRESERVEDATABASE

A <b>VT_BOOL</b> value that specifies whether to preserve an existing database. This is relevant under the following conditions:

<ul>
<li>A CA 

was previously installed (and later uninstalled) on this computer.</li>
<li>An existing key (and its associated certificate) is being used for installation.</li>
<li>A database exists in the given database directory.</li>
</ul>

### -field ENUM_SETUPPROP_DATABASEDIRECTORY

A <b>VT_BSTR</b> value that specifies the path of the directory where CA database files are stored after installation. The default path is %SystemRoot%\System32\Certlog\.


### -field ENUM_SETUPPROP_LOGDIRECTORY

A <b>VT_BSTR</b> value that specifies the path of the directory where CA database log files are stored after installation. The default path is %SystemRoot%\System32\Certlog\.


### -field ENUM_SETUPPROP_SHAREDFOLDER

This value is not used and is reserved for future use.


### -field ENUM_SETUPPROP_PARENTCAMACHINE

A <b>VT_BSTR</b> value that specifies the name of the computer that is hosting the parent CA. This value is only applicable if a subordinate CA is being installed. There is no default value.


### -field ENUM_SETUPPROP_PARENTCANAME

A <b>VT_BSTR</b> value that specifies the name of the parent CA. This value is only applicable if a subordinate CA is being installed. There is no default value.


### -field ENUM_SETUPPROP_REQUESTFILE

A <b>VT_BSTR</b> value that specifies the file path to use to save a subordinate CA request, so that it can be submitted later to the parent CA. The default value is %SystemDrive%\<i>DNSMachineName</i>_<i>CAName</i>.req.


### -field ENUM_SETUPPROP_WEBCAMACHINE

A <b>VT_BSTR</b> value that specifies the name of the computer that is hosting the CA. This value is only applicable if support for the Certification Authority Web Enrollment role is being installed. There is no default value.


### -field ENUM_SETUPPROP_WEBCANAME

A <b>VT_BSTR</b> value that specifies the name of the CA. This value is only applicable if support for the Certification Authority Web Enrollment role is being installed. There is no default value.

