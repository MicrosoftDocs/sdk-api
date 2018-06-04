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

# LPDSENUMATTRIBUTES callback function


## -description


The <b>DSEnumAttributesCallback</b> function is an application-defined callback function that is called once for each attribute enumerated by the <a href="https://msdn.microsoft.com/78b8e280-454c-4db7-9037-ea7e42798323">IDsDisplaySpecifier::EnumClassAttributes</a> method. A pointer to this function is supplied as the <i>pcbEnum</i> parameter in <b>IDsDisplaySpecifier::EnumClassAttributes</b>. <b>DSEnumAttributesCallback</b> is a placeholder for the application-defined function name.


## -parameters




### -param lParam

Contains an application-defined  parameter  passed as the <i>lParam</i> parameter to the <a href="https://msdn.microsoft.com/78b8e280-454c-4db7-9037-ea7e42798323">IDsDisplaySpecifier::EnumClassAttributes</a> method.


### -param pszAttributeName

Pointer to a null-terminated Unicode string that contains the LDAP name of the attribute.


### -param pszDisplayName

Pointer to a null-terminated Unicode string that contains the localized name of the attribute.


### -param dwFlags

Contains a set of flags that define the behavior or state of the attribute. This can be zero or the following value:



#### DSECAF_NOTLISTED

The attribute is hidden in the user interface.


## -returns



Returns <b>S_OK</b> to continue the enumeration or any failure code, such as <b>E_FAIL</b>, to terminate the enumeration.




## -see-also




<a href="https://msdn.microsoft.com/78b8e280-454c-4db7-9037-ea7e42798323">IDsDisplaySpecifier::EnumClassAttributes</a>
 

 

