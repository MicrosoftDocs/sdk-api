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

# ldap_escape_filter_element function


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




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/822411b7-fc49-4b93-8e54-353350ed5de9">Return Values</a>
 

 

