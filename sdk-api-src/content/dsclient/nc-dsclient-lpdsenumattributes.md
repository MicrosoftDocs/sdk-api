---
UID: NC:dsclient.LPDSENUMATTRIBUTES
title: LPDSENUMATTRIBUTES (dsclient.h)
description: The DSEnumAttributesCallback function is an application-defined callback function that is called once for each attribute enumerated by the IDsDisplaySpecifier::EnumClassAttributes method.
helpviewer_keywords: ["DSECAF_NOTLISTED","DSEnumAttributesCallback","DSEnumAttributesCallback callback","DSEnumAttributesCallback callback function [Active Directory]","LPDSENUMATTRIBUTES","LPDSENUMATTRIBUTES callback function [Active Directory]","ad.dsenumattributescallback","dsclient/DSEnumAttributesCallback"]
old-location: ad\dsenumattributescallback.htm
tech.root: ad
ms.assetid: f4f35119-9ffc-4fe9-aea1-2d4a5d4edd0b
ms.date: 12/05/2018
ms.keywords: DSECAF_NOTLISTED, DSEnumAttributesCallback, DSEnumAttributesCallback callback, DSEnumAttributesCallback callback function [Active Directory], LPDSENUMATTRIBUTES, LPDSENUMATTRIBUTES callback function [Active Directory], ad.dsenumattributescallback, dsclient/DSEnumAttributesCallback
req.header: dsclient.h
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LPDSENUMATTRIBUTES
 - dsclient/LPDSENUMATTRIBUTES
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Dsclient.h
api_name:
 - LPDSENUMATTRIBUTES
---

# LPDSENUMATTRIBUTES callback function


## -description

The <b>DSEnumAttributesCallback</b> function is an application-defined callback function that is called once for each attribute enumerated by the <a href="/windows/desktop/api/dsclient/nf-dsclient-idsdisplayspecifier-enumclassattributes">IDsDisplaySpecifier::EnumClassAttributes</a> method. A pointer to this function is supplied as the <i>pcbEnum</i> parameter in <b>IDsDisplaySpecifier::EnumClassAttributes</b>. <b>DSEnumAttributesCallback</b> is a placeholder for the application-defined function name.

## -parameters

### -param lParam

Contains an application-defined  parameter  passed as the <i>lParam</i> parameter to the <a href="/windows/desktop/api/dsclient/nf-dsclient-idsdisplayspecifier-enumclassattributes">IDsDisplaySpecifier::EnumClassAttributes</a> method.

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

<a href="/windows/desktop/api/dsclient/nf-dsclient-idsdisplayspecifier-enumclassattributes">IDsDisplaySpecifier::EnumClassAttributes</a>