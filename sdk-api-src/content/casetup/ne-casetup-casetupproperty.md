---
UID: NE:casetup.__MIDL___MIDL_itf_casetup_0000_0002_0001
title: CASetupProperty (casetup.h)
description: Specifies a property type for setup and configuration of a certification authority (CA) role when using the ICertSrvSetup interface.
helpviewer_keywords: ["CASetupProperty","CASetupProperty enumeration [Security]","ENUM_SETUPPROP_CADSSUFFIX","ENUM_SETUPPROP_CAKEYINFORMATION","ENUM_SETUPPROP_CANAME","ENUM_SETUPPROP_CATYPE","ENUM_SETUPPROP_DATABASEDIRECTORY","ENUM_SETUPPROP_EXPIRATIONDATE","ENUM_SETUPPROP_INTERACTIVE","ENUM_SETUPPROP_INVALID","ENUM_SETUPPROP_LOGDIRECTORY","ENUM_SETUPPROP_PARENTCAMACHINE","ENUM_SETUPPROP_PARENTCANAME","ENUM_SETUPPROP_PRESERVEDATABASE","ENUM_SETUPPROP_REQUESTFILE","ENUM_SETUPPROP_SHAREDFOLDER","ENUM_SETUPPROP_VALIDITYPERIOD","ENUM_SETUPPROP_VALIDITYPERIODUNIT","ENUM_SETUPPROP_WEBCAMACHINE","ENUM_SETUPPROP_WEBCANAME","casetup/CASetupProperty","casetup/ENUM_SETUPPROP_CADSSUFFIX","casetup/ENUM_SETUPPROP_CAKEYINFORMATION","casetup/ENUM_SETUPPROP_CANAME","casetup/ENUM_SETUPPROP_CATYPE","casetup/ENUM_SETUPPROP_DATABASEDIRECTORY","casetup/ENUM_SETUPPROP_EXPIRATIONDATE","casetup/ENUM_SETUPPROP_INTERACTIVE","casetup/ENUM_SETUPPROP_INVALID","casetup/ENUM_SETUPPROP_LOGDIRECTORY","casetup/ENUM_SETUPPROP_PARENTCAMACHINE","casetup/ENUM_SETUPPROP_PARENTCANAME","casetup/ENUM_SETUPPROP_PRESERVEDATABASE","casetup/ENUM_SETUPPROP_REQUESTFILE","casetup/ENUM_SETUPPROP_SHAREDFOLDER","casetup/ENUM_SETUPPROP_VALIDITYPERIOD","casetup/ENUM_SETUPPROP_VALIDITYPERIODUNIT","casetup/ENUM_SETUPPROP_WEBCAMACHINE","casetup/ENUM_SETUPPROP_WEBCANAME","security.icertsrvsetup_casetupproperty"]
old-location: security\icertsrvsetup_casetupproperty.htm
tech.root: security
ms.assetid: 2245ad2f-89ca-4478-91d0-cbd7a0648479
ms.date: 12/05/2018
ms.keywords: CASetupProperty, CASetupProperty enumeration [Security], ENUM_SETUPPROP_CADSSUFFIX, ENUM_SETUPPROP_CAKEYINFORMATION, ENUM_SETUPPROP_CANAME, ENUM_SETUPPROP_CATYPE, ENUM_SETUPPROP_DATABASEDIRECTORY, ENUM_SETUPPROP_EXPIRATIONDATE, ENUM_SETUPPROP_INTERACTIVE, ENUM_SETUPPROP_INVALID, ENUM_SETUPPROP_LOGDIRECTORY, ENUM_SETUPPROP_PARENTCAMACHINE, ENUM_SETUPPROP_PARENTCANAME, ENUM_SETUPPROP_PRESERVEDATABASE, ENUM_SETUPPROP_REQUESTFILE, ENUM_SETUPPROP_SHAREDFOLDER, ENUM_SETUPPROP_VALIDITYPERIOD, ENUM_SETUPPROP_VALIDITYPERIODUNIT, ENUM_SETUPPROP_WEBCAMACHINE, ENUM_SETUPPROP_WEBCANAME, casetup/CASetupProperty, casetup/ENUM_SETUPPROP_CADSSUFFIX, casetup/ENUM_SETUPPROP_CAKEYINFORMATION, casetup/ENUM_SETUPPROP_CANAME, casetup/ENUM_SETUPPROP_CATYPE, casetup/ENUM_SETUPPROP_DATABASEDIRECTORY, casetup/ENUM_SETUPPROP_EXPIRATIONDATE, casetup/ENUM_SETUPPROP_INTERACTIVE, casetup/ENUM_SETUPPROP_INVALID, casetup/ENUM_SETUPPROP_LOGDIRECTORY, casetup/ENUM_SETUPPROP_PARENTCAMACHINE, casetup/ENUM_SETUPPROP_PARENTCANAME, casetup/ENUM_SETUPPROP_PRESERVEDATABASE, casetup/ENUM_SETUPPROP_REQUESTFILE, casetup/ENUM_SETUPPROP_SHAREDFOLDER, casetup/ENUM_SETUPPROP_VALIDITYPERIOD, casetup/ENUM_SETUPPROP_VALIDITYPERIODUNIT, casetup/ENUM_SETUPPROP_WEBCAMACHINE, casetup/ENUM_SETUPPROP_WEBCANAME, security.icertsrvsetup_casetupproperty
req.header: casetup.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: CASetupProperty
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_casetup_0000_0002_0001
 - casetup/__MIDL___MIDL_itf_casetup_0000_0002_0001
 - CASetupProperty
 - casetup/CASetupProperty
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Casetup.h
api_name:
 - CASetupProperty
---

# CASetupProperty enumeration


## -description

The <b>CASetupProperty</b> enumeration specifies a property type for setup and configuration of a <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> (CA) role when using the <a href="/windows/desktop/api/casetup/nn-casetup-icertsrvsetup">ICertSrvSetup</a> interface.

## -enum-fields

### -field ENUM_SETUPPROP_INVALID:-1

A value that specifies a property type that is not valid.

### -field ENUM_SETUPPROP_CATYPE:0

A <b>VT_I4</b> value that specifies a value of the <a href="/windows/desktop/api/certsrv/ne-certsrv-enum_catypes">ENUM_CATYPES</a> enumeration.

If the computer is not joined to a domain, or the caller

is not an Enterprise or Domain administrator but is a local administrator, the default value is <b>ENUM_STANDALONE_ROOTCA</b>. If the computer is joined to a domain, the caller is an Enterprise or Domain administrator, and an enterprise root CA already exists, the default is <b>ENUM_ENTERPRISE_SUBCA</b>, or if no enterprise root CA exists, the default value is <b>ENUM_ENTERPRISE_ROOTCA</b>.

### -field ENUM_SETUPPROP_CAKEYINFORMATION:1

A <b>VT_DISPATCH</b> value, in the form of a <b>CCertSrvSetupKeyInformation</b>  object, that specifies the <a href="/windows/desktop/SecGloss/p-gly">private key</a> information used for a CA certificate. By default, setup generates a new key

with a 2048-bit key length for root and subordinate CAs using "Microsoft

Strong Cryptographic Provider."

### -field ENUM_SETUPPROP_INTERACTIVE:2

A <b>VT_BOOL</b> value that indicates whether the <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP) is allowed to interact with the desktop. The default is false.

### -field ENUM_SETUPPROP_CANAME:3

A <b>VT_BSTR</b> value that contains the common name for the CA. By default, the common 

name is <i>DomainName</i>-<i>LocalComputerName</i>-<i>CAName</i>.

### -field ENUM_SETUPPROP_CADSSUFFIX:4

A <b>VT_BSTR</b> value that contains the distinguished name suffix for a CA name.

### -field ENUM_SETUPPROP_VALIDITYPERIOD:5

A <b>VT_I4</b> value that specifies the number of units in the validity period as specified by the <b>ENUM_SETUPPROP_VALIDITYPERIODUNIT</b> property type. For a subordinate CA, the validity period is determined by the parent CA.

### -field ENUM_SETUPPROP_VALIDITYPERIODUNIT:6

A <b>VT_I4</b> value that specifies a value of the <a href="/windows/desktop/api/celib/ne-celib-enum_period">ENUM_PERIOD</a> enumeration that indicates the time units of the validity period. For a subordinate CA, the validity period time unit is determined by the parent CA.

### -field ENUM_SETUPPROP_EXPIRATIONDATE:7

A <b>VT_BSTR</b> value that specifies the expected expiration date of the root CA certificate based on the current time, validity period, and validity period unit. For a subordinate CA, the expiration date is

determined by its parent CA.

### -field ENUM_SETUPPROP_PRESERVEDATABASE:8

A <b>VT_BOOL</b> value that specifies whether to preserve an existing database. This is relevant under the following conditions:

<ul>
<li>A CA 

was previously installed (and later uninstalled) on this computer.</li>
<li>An existing key (and its associated certificate) is being used for installation.</li>
<li>A database exists in the given database directory.</li>
</ul>

### -field ENUM_SETUPPROP_DATABASEDIRECTORY:9

A <b>VT_BSTR</b> value that specifies the path of the directory where CA database files are stored after installation. The default path is %SystemRoot%\System32\Certlog\.

### -field ENUM_SETUPPROP_LOGDIRECTORY:10

A <b>VT_BSTR</b> value that specifies the path of the directory where CA database log files are stored after installation. The default path is %SystemRoot%\System32\Certlog\.

### -field ENUM_SETUPPROP_SHAREDFOLDER:11

This value is not used and is reserved for future use.

### -field ENUM_SETUPPROP_PARENTCAMACHINE:12

A <b>VT_BSTR</b> value that specifies the name of the computer that is hosting the parent CA. This value is only applicable if a subordinate CA is being installed. There is no default value.

### -field ENUM_SETUPPROP_PARENTCANAME:13

A <b>VT_BSTR</b> value that specifies the name of the parent CA. This value is only applicable if a subordinate CA is being installed. There is no default value.

### -field ENUM_SETUPPROP_REQUESTFILE:14

A <b>VT_BSTR</b> value that specifies the file path to use to save a subordinate CA request, so that it can be submitted later to the parent CA. The default value is %SystemDrive%&#92;&#92;<i>DNSMachineName</i>_<i>CAName</i>.req.

### -field ENUM_SETUPPROP_WEBCAMACHINE:15

A <b>VT_BSTR</b> value that specifies the name of the computer that is hosting the CA. This value is only applicable if support for the Certification Authority Web Enrollment role is being installed. There is no default value.

### -field ENUM_SETUPPROP_WEBCANAME:16

A <b>VT_BSTR</b> value that specifies the name of the CA. This value is only applicable if support for the Certification Authority Web Enrollment role is being installed. There is no default value.
