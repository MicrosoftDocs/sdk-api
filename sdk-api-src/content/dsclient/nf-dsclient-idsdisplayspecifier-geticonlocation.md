---
UID: NF:dsclient.IDsDisplaySpecifier.GetIconLocation
title: IDsDisplaySpecifier::GetIconLocation (dsclient.h)
description: Obtains the icon location for a given object class.
helpviewer_keywords: ["DSGIF_DEFAULTISCONTAINER","DSGIF_GETDEFAULTICON","DSGIF_ISDISABLED","DSGIF_ISNORMAL","DSGIF_ISOPEN","GetIconLocation","GetIconLocation method [Active Directory]","GetIconLocation method [Active Directory]","IDsDisplaySpecifier interface","IDsDisplaySpecifier interface [Active Directory]","GetIconLocation method","IDsDisplaySpecifier.GetIconLocation","IDsDisplaySpecifier::GetIconLocation","_glines_idsdisplayspecifier_geticonlocation","ad.idsdisplayspecifier__geticonlocation","ad.idsdisplayspecifier_geticonlocation","dsclient/IDsDisplaySpecifier::GetIconLocation"]
old-location: ad\idsdisplayspecifier_geticonlocation.htm
tech.root: ad
ms.assetid: a5e65bde-aa2d-47e0-8cfc-062b14da3e87
ms.date: 12/05/2018
ms.keywords: DSGIF_DEFAULTISCONTAINER, DSGIF_GETDEFAULTICON, DSGIF_ISDISABLED, DSGIF_ISNORMAL, DSGIF_ISOPEN, GetIconLocation, GetIconLocation method [Active Directory], GetIconLocation method [Active Directory],IDsDisplaySpecifier interface, IDsDisplaySpecifier interface [Active Directory],GetIconLocation method, IDsDisplaySpecifier.GetIconLocation, IDsDisplaySpecifier::GetIconLocation, _glines_idsdisplayspecifier_geticonlocation, ad.idsdisplayspecifier__geticonlocation, ad.idsdisplayspecifier_geticonlocation, dsclient/IDsDisplaySpecifier::GetIconLocation
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
req.dll: Dsadmin.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDsDisplaySpecifier::GetIconLocation
 - dsclient/IDsDisplaySpecifier::GetIconLocation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dsadmin.dll
api_name:
 - IDsDisplaySpecifier.GetIconLocation
---

# IDsDisplaySpecifier::GetIconLocation


## -description

The <b>IDsDisplaySpecifier::GetIconLocation</b> method obtains the icon location for a given object class. The icon location includes the filename and resource identifier.

## -parameters

### -param pszObjectClass [in]

Pointer to a null-terminated Unicode string that contains the name of the object class for which to obtain the icon location. Examples of the object class name are "user" and "container".

### -param dwFlags [in]

Contains a set of flags that indicate the type of icon to retrieve. This can be a combination of one or more of the following.



#### DSGIF_ISNORMAL

Obtains the normal  icon for the object class.



#### DSGIF_ISOPEN

Obtains the open  icon, such as an open folder, for the object class. If the object class does not have an open icon, this method attempts to obtain the normal icon for the object class.



#### DSGIF_ISDISABLED

Obtains the disabled icon, such as a disabled user, for the object class. If the object class does not have a disabled  icon, this method attempts to obtain the normal icon for the object class.



#### DSGIF_GETDEFAULTICON

If no icon can be found for the object class, this method returns a default icon. If this flag is not specified and no icon can be found for the object class, this method returns <b>NULL</b>.



#### DSGIF_DEFAULTISCONTAINER

If no icon can be found for the object class, this method returns the container icon as the default icon. If this flag is not specified and no icon can be found for the object class, this method returns <b>NULL</b>.

### -param pszBuffer [in, out]

Pointer to a wide character buffer that receives the path and file name of the file that contains the icon. This buffer must be at least <i>cchBuffer</i> wide characters in length.

### -param cchBuffer [in]

Contains the size of the <i>pszBuffer</i> buffer, in wide characters, including the terminating <b>NULL</b> character. If the file name exceeds this number of characters, the file name is truncated.

### -param presid [in, out]

Pointer to an <b>INT</b> value that  receives the resource identifier or index of the icon. If this value is positive, the value is the index of the icon in the file. If this value is negative, the absolute value of this value is the resource identifier of the icon in the file.

## -returns

Returns a standard <b>HRESULT</b> value including the following.

## -see-also

<a href="/windows/desktop/AD/display-interfaces-in-active-directory-domain-services">Display Interfaces in Active Directory Domain Services</a>



<a href="/windows/desktop/api/dsclient/nn-dsclient-idsdisplayspecifier">IDsDisplaySpecifier</a>



<a href="/windows/desktop/api/dsclient/nf-dsclient-idsdisplayspecifier-geticon">IDsDisplaySpecifier::GetIcon</a>