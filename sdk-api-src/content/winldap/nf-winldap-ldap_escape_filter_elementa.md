---
UID: NF:winldap.ldap_escape_filter_elementA
title: ldap_escape_filter_elementA function
author: windows-sdk-content
description: The ldap_escape_filter_element function converts a filter element to a null-terminated character string that can be passed safely in a search filter.
old-location: ldap\ldap_escape_filter_element.htm
tech.root: ldap
ms.assetid: d3bc558c-7327-400e-a436-35adae8fc302
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "_ldap_ldap_escape_filter_element, ldap.ldap__escape__filter__element, ldap.ldap_escape_filter_element, ldap_escape_filter_element, ldap_escape_filter_element function [LDAP], ldap_escape_filter_elementA, ldap_escape_filter_elementW, winldap/ldap_escape_filter_element, winldap/ldap_escape_filter_elementA, winldap/ldap_escape_filter_elementW"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ldap_escape_filter_elementW (Unicode) and ldap_escape_filter_elementA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wldap32.lib
req.dll: Wldap32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wldap32.dll
api_name:
 - ldap_escape_filter_element
 - ldap_escape_filter_elementA
 - ldap_escape_filter_elementW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ldap_escape_filter_elementA function


## -description


The <b>ldap_escape_filter_element</b> function converts a filter element to a null-terminated character  string that can be passed safely in a search filter.


## -parameters




### -param sourceFilterElement [in]

A pointer to a null-terminated string that contains the filter element to convert.


### -param sourceLength [in]

The length, in bytes, of the source filter element.


### -param destFilterElement [out]

A pointer to a null-terminated character string.


### -param destLength [in]

The length, in bytes, of the <i>destFilterElement</i> buffer.


## -returns



If the function succeeds, the return value is <b>LDAP_SUCCESS</b>.

If the function fails, it returns an error code. See 
<a href="https://msdn.microsoft.com/822411b7-fc49-4b93-8e54-353350ed5de9">Return Values</a> for more information.




## -remarks



The <b>ldap_escape_filter_element</b> function allows you to use raw binary data in search filters. For example, you can use this function to specify a certificate or a JPEG image as the attribute to match.

Call <b>ldap_escape_filter_element</b> with the <i>sourceFilterElement</i> parameter pointing to raw data and <i>sourceLength</i> set appropriately to the length of data. If the <i>destFilterElement</i> parameter is <b>NULL</b>, then the return value is the length required for the output buffer. If <i>destFilterElement</i> is not <b>NULL</b>, then the function copies the source into the destination buffer and ensures that it is of a safe format. Then insert the destination buffer into your search filter after the "attributetype=" filter element.

<div class="alert"><b>Note</b>  Do not call <b>ldap_escape_filter_element</b> for attribute values that are strings, as the run time does not perform any conversion from UTF-8 format. Use this function only for attribute elements that are raw binary data.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/7a0040ea-f8f3-4378-8371-49768714d762">Functions</a>



<a href="https://msdn.microsoft.com/822411b7-fc49-4b93-8e54-353350ed5de9">Return Values</a>
 

 

