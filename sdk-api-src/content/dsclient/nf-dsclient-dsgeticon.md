---
UID: NF:dsclient.DsGetIcon
title: DsGetIcon function (dsclient.h)
description: Obtains the icon for a given object class.
helpviewer_keywords: ["DSGIF_DEFAULTISCONTAINER","DSGIF_GETDEFAULTICON","DSGIF_ISDISABLED","DSGIF_ISNORMAL","DSGIF_ISOPEN","DsGetIcon","DsGetIcon function [Active Directory]","ad.dsgeticon","dsclient/DsGetIcon"]
old-location: ad\dsgeticon.htm
tech.root: ad
ms.assetid: eee18c78-aefa-4f09-9361-91893502efec
ms.date: 12/05/2018
ms.keywords: DSGIF_DEFAULTISCONTAINER, DSGIF_GETDEFAULTICON, DSGIF_ISDISABLED, DSGIF_ISNORMAL, DSGIF_ISOPEN, DsGetIcon, DsGetIcon function [Active Directory], ad.dsgeticon, dsclient/DsGetIcon
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
req.lib: Dsuiext.lib
req.dll: Dsuiext.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DsGetIcon
 - dsclient/DsGetIcon
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dsuiext.dll
api_name:
 - DsGetIcon
---

# DsGetIcon function


## -description

The <b>DsGetIcon</b> function obtains the icon for a given object class. This function is obsolete. New applications should use the <a href="/windows/desktop/api/dsclient/nf-dsclient-idsdisplayspecifier-geticon">IDsDisplaySpecifier::GetIcon</a> method to perform this function.

## -parameters

### -param dwFlags [in]

Contains a set of flags that indicate the type of icon to retrieve. This can be a combination of one or more of the following values.



#### DSGIF_ISNORMAL

Obtains the normal  icon for the object class.



#### DSGIF_ISOPEN

Obtains the open  icon, such as an open folder, for the object class. If the object class does not have an open icon, this function attempts to obtain the normal icon for the object class.



#### DSGIF_ISDISABLED

Obtains the disabled icon, such as a disabled user, for the object class. If the object class does not have a disabled  icon, this function attempts to obtain the normal icon for the object class.



#### DSGIF_GETDEFAULTICON

If no icon can be found for the object class, this function will return a default icon. If this flag is not specified and no icon can be found for the object class, this function returns <b>NULL</b>.



#### DSGIF_DEFAULTISCONTAINER

If no icon can be found for the object class, this function returns the container icon as the default icon. If this flag is not specified and no icon can be found for the object class, this function returns <b>NULL</b>.

### -param pszObjectClass [in]

Pointer to a null-terminated Unicode string that contains the name of the object class to retrieve the icon for. Examples of the object class name are "user" and "container".

### -param cxImage [in]

Contains the desired width, in pixels, of the icon. This function retrieves the icon that most closely matches this width.

### -param cyImage [in]

Contains the desired height, in pixels, of the icon. This function retrieves the icon that most closely matches this height.

## -returns

Returns a handle to the icon if successful or <b>NULL</b> otherwise. The caller must destroy this icon when it is no longer required by passing this handle to <a href="/windows/desktop/api/winuser/nf-winuser-destroyicon">DestroyIcon</a>.

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-destroyicon">DestroyIcon</a>



<a href="/windows/desktop/api/dsclient/nf-dsclient-idsdisplayspecifier-geticon">IDsDisplaySpecifier::GetIcon</a>