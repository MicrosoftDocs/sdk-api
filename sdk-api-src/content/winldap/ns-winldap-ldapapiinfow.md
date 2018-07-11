---
UID: NS:winldap.ldapapiinfoW
title: ldapapiinfoW
author: windows-sdk-content
description: Retrieves data about the API and implementations used.
old-location: ldap\ldapapiinfo.htm
old-project: ldap
ms.assetid: 9175224c-82f0-4f22-9975-b1d7a332c3df
ms.author: windowssdkdev
ms.date: 06/14/2018
ms.keywords: LDAPAPIInfo, LDAPAPIInfo structure [LDAP], LDAPAPIInfoA, LDAPAPIInfoW, ldap.ldapapiinfo, ldapapiinfoW, winldap/LDAPAPIInfo, winldap/LDAPAPIInfoA, winldap/LDAPAPIInfoW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: LDAPAPIInfoW (Unicode) and LDAPAPIInfoA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: LDAPAPIInfoW
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winldap.h
api_name:
 - LDAPAPIInfo
 - LDAPAPIInfoA
 - LDAPAPIInfoW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# ldapapiinfoW structure


## -description


The <b>LDAPAPIInfo</b> structure retrieves data about the API and implementations used.


## -struct-fields




### -field ldapai_info_version

The version of this structure, which must be set to <b>LDAP_API_INFO_VERSION</b> before a call to <a href="https://msdn.microsoft.com/e07c2c3d-8099-4f9c-9ee7-26c1287110d5">ldap_get_option</a>.


### -field ldapai_api_version

The current revision number of this LDAP API library.


### -field ldapai_protocol_version

The latest LDAP version supported by this LDAP API library.


### -field ldapai_extensions

Pointer to an array of null-terminated strings that indicate what API extensions are supported.


### -field ldapai_vendor_name

Pointer to a null-terminated string that contains the name of the API vendor.  This implementation returns the string ""Microsoft Corporation."".


### -field ldapai_vendor_version

The API vendor version number. This implementation returns an integer value in the format of MMnn, where MM is the major version number * 100, and nn is the minor version number.  For example, version 5.10 is returned as 510.


## -remarks



A pointer to this structure is passed with the <a href="https://msdn.microsoft.com/a968e66d-933f-44b7-b74d-d18a92d7de3f">LDAP_OPT_API_INFO</a> session option, to <a href="https://msdn.microsoft.com/e07c2c3d-8099-4f9c-9ee7-26c1287110d5">ldap_get_option</a>, to retrieve data about this LDAP API library.  The data returned includes a list of any API extensions supported by the implementation. When the structure data is no longer required, the caller must free the individual strings and string arrays returned in this structure by using the <a href="https://msdn.microsoft.com/3256a202-4245-4bea-a66c-0f28bfe2ef7e">ldap_memfree</a> and <a href="https://msdn.microsoft.com/67c9f04c-4b8e-4e97-902d-fceccf27f522">ldap_value_free</a> functions.




## -see-also




<a href="https://msdn.microsoft.com/a968e66d-933f-44b7-b74d-d18a92d7de3f">Session Options</a>



<a href="https://msdn.microsoft.com/e07c2c3d-8099-4f9c-9ee7-26c1287110d5">ldap_get_option</a>



<a href="https://msdn.microsoft.com/3256a202-4245-4bea-a66c-0f28bfe2ef7e">ldap_memfree</a>



<a href="https://msdn.microsoft.com/67c9f04c-4b8e-4e97-902d-fceccf27f522">ldap_value_free</a>
 

 

